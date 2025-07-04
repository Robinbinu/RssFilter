To make it easier to utilize Alibaba Cloud Function Compute's free tier, this project extracts the [RSS Filter](https://pyrsshub.vercel.app/feeds) feature from the [RSSHub-Python](https://github.com/hillerliao/RSSHub-python) project and adapts it for Alibaba Cloud Function Compute.

Project address: `https://github.com/hillerliao/RssFilter`

Deployment instructions are as follows:

## 1. Create Service

1. Go to [Alibaba Cloud Function Compute](https://fcnext.console.aliyun.com/overview) dashboard and click "Create Service".

![Alibaba Cloud Function Compute Overview](https://github.com/easychen/wecomchan/raw/main/python-aliyunfc/pic/image-20220205142747826.png)

2. Enter a service name (e.g., `RssFilter`) and click "Confirm".

![Alibaba Cloud Function Compute - Create Service](https://raw.githubusercontent.com/hillerliao/img/main/20220918133712.png)

## 2. Configure Function

3. Configure the function.

3.1 Enter the newly created service and click `Create Function`;  
3.2 Select `Create with Custom Runtime`, enter function name (e.g., `main`);  
3.3 For code upload method, choose `Upload ZIP Package`, download and upload the [filter ZIP package](https://github.com/hillerliao/RssFilter/blob/main/func-code-4-RSSFilter.zip)`func-code-4-RSSFilter.zip` from this repository;  
3.4 Enter `python app.py` as the startup command;  

Click `Create`.

![Alibaba Cloud Function Compute - Configure Function](https://raw.githubusercontent.com/hillerliao/img/main/20220918134114.png)

## 3. Get Access Address

4. Obtain the test address with path and parameters, such as `/filter?feed=<RSS URL>&include_title=<filter keyword>`. Supported parameters are the same as RSSHub-Python's [RSS Filter parameters](https://pyrsshub.vercel.app/feeds).

![Alibaba Cloud Function Compute - Get Public Function Address](https://raw.githubusercontent.com/hillerliao/img/main/20220918134337.png)

Example:

`http://<testing sub domain for fc>.cn-beijing.functioncompute.com/filter?feed=https://sspai.com/feed&include_title=派评`

5. After successful testing, click `Deploy Code` to complete deployment.

![Alibaba Cloud Function Compute - Online Editor](https://raw.githubusercontent.com/hillerliao/img/main/20220918134819.png)

## 4. Original Purpose of RSS Filter

Reflecting on my original intention for creating the RSS Filter: to improve information acquisition efficiency.

For example, for some RSS feeds, I only care about content containing specific keywords; for others, I want to exclude content with certain advertising keywords. The RSS Filter can satisfy these needs.

If you find this project useful, you can buy me a coffee.

![Personal WeChat Payment QR Code - Zhihai](https://raw.githubusercontent.com/hillerliao/img/main/IMG_0096%20copy.jpg)

For improvement suggestions, feel free to contact me. WeChat: `hillerliao`.
