# 1. background(Runbo)

Hello everyone, here is team with Runbo, Zewen and Yihao. Today our topic is the vulnerability  of Qualcomm Mobile Station Modem.

Before we talk about this case, let me give you a brief introduction to our protagonist(prōˈtaɡənəst) today, Qualcomm. 

## 1.1 What is Qualcomm？

So what is Qualcomm? Qualcomm is an American multinational corporation headquartered in San Diego, California, established in July 1985. It creates semiconductors, software, and services related to wireless technology. It is in the leading position in CDMA technology, and is the world's largest wireless chip manufacturer. Qualcomm's customers and partners include not only the world's leading manufacturers of mobile phones, tablets, routers and systems, but also the world's leading wireless operators. Most Android phone manufacturers such as Samsung, Google, One Plus, Xiaomi are using Qualcomm's chips for their products. Today's case is related to the chip developed by Qualcomm.[^intro of qualcomm]

## 1.2 What happened in this case?

So what happened in this case? In brief, there is a Vulnerability in the Mobile Station Modem designed by Qualcomm. MSM is a series of Qualcomm chips, which is actually a series of mobile phone processors with built-in baseband. The Vulnerability is in the interface of the MSM, which is called QMI. Where QMI is a proprietary(p(r)əˈprīəˌterēv) protocol used to communicate between software components in the modem and other peripheral subsystems. [^case introduction]

## 1.3 Who can uses and what can they do?

Absolutely, anyone or hackers who want to steal personal information can use this Vulnerability. 

An attacker could use this Vulnerability to remotely attack an Android mobile device by injecting a malicious or trojanized(戳着奶子的) Android application into the phone's MSM components. 

Then the hacker can get the ability to execute code and then get access to the mobile user's call history ,text messages, and wiretap phone calls, etc. In addition, hackers could also use this Vulnerability to unlock SIM cards, thereby removing restrictions imposed by service providers on mobile devices.

Since Qualcomm's MSM chips are used in high-end smartphones sold by Google, Samsung, LG, Xiaomi, and One Plus, this Vulnerability could affect more that 30 percent of Android phones.[^more intro]

Zewen will introduce more detail about this Vulnerability. 



# 2. Principle (Zewen) 





# 3. Impact and prevention（Yihao）



## 3.1 Impact

As runbo said, Qualcomm is one of the top telecommunications technology research and development companies. If its chips suffer from security problems, it will affect more than 30% of mobile phone users. This will be a disaster. How to avoid this problem should be Everyone needs to consider.

An attacker could exploit this vulnerability to remotely attack a mobile device through a malicious or trojanized Android application. "Assuming a malicious app was running on the phone, it could exploit this vulnerability to 'hide' itself in the modem chip, making it invisible to all the security measures currently on the phone."

After being targeted by hackers, the user's text messages, call records, call information, and even unlocking the user identification module on the mobile device, storing the user's network authentication information and contact information will no longer be their own secrets.

Imagine if my phone was hacked to steal all my stuff and I would be as naked as in a washroom with no secrets at all.

In order to avoid it, what should we do, and what should we do. 



## 3.2 Prevention

1. Upgrade the latest operating system and virtualization software patches

2. Update the latest browser patch

3. Wait or ask your cloud service provider to update the virtualization system patch in time;

4. Install security software. 

   As a user, either the mobile phone operating system and chips are from the Apple mobile phone camp, which is developed by itself and the ecosystem is relatively closed, or, beware of all application downloads and installations from unknown sources.

​        

# Reference

[^intro of qualcomm]: https://en.wikipedia.org/wiki/Qualcomm, https://baike.baidu.com/item/%E9%AB%98%E9%80%9A/3119501, https://product.pconline.com.cn/itbk/company/subItcom/1111/2574925.html, https://wiki.mbalib.com/wiki/%E7%BE%8E%E5%9B%BD%E9%AB%98%E9%80%9A%E5%85%AC%E5%8F%B8, https://www.mg21.com/qcom.html



[^case introduction]: https://vulmon.com/vulnerabilitydetails?qid=CVE-2020-11292, https://cisomag.eccouncil.org/vulnerability-in-qualcomm-msm-chip/, https://research.checkpoint.com/2021/security-probe-of-qualcomm-msm/, https://www.cpomagazine.com/cyber-security/security-vulnerability-in-qualcomm-chips-affects-nearly-40-percent-of-smartphones-compromises-flagship-android-phones/, https://threatpost.com/qualcomm-chip-bug-android-eavesdropping/165934/, https://www.sohu.com/a/465212446_114760



[^more intro]: https://www.sohu.com/a/465212446_114760, https://m.freebuf.com/articles/272066.html, http://finance.sina.com.cn/tech/csj/2021-05-09/doc-ikmxzfmm1379410.shtml, https://www.wangan.com/articles/4546,https://www.secrss.com/articles/31011
