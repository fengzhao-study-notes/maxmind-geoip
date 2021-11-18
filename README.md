# maxmind-geoip

https://blog.maxmind.com/2019/12/18/significant-changes-to-accessing-and-using-geolite2-databases/

# License

This repository includes [GeoLite2](https://dev.maxmind.com/geoip/geoip2/geolite2/) data created by [MaxMind](https://www.maxmind.com).


# GEOIP简介

Geo是geographic的缩写，意思是地理的，GeoIP即为IP地理位置数据库，可以根据IP获得地理位置信息。

maxmind提供了免费的可在本地部署的geo-ip数据库（GeoLite2）（mmdb以及csv格式），和geo-ip查询api服务





GeoLite2是GeoIP2的免费版本，与GeoIP2数据库相比准确性较差。

GeoLite2数据库每周更新国家、城市和自治系统编号信息，更新时间为每周二。

IP地理定位本质上是不精确的，地点通常靠近人口中心。

GeoIP数据库提供的任何位置不应用于识别特定地址或家庭，使用精度半径作为IP地址返回的纬度和经度坐标的地理定位精度指示，IP地址的实际位置可能在这个半径和经纬度坐标所定义的区域内。




# Maxmind GEOIP简介

MaxMind介绍MaxMind成立于2002年，在提供几何定位和在线欺诈工具方面MaxMind处于领先地位。MaxMind是通过GeoIP品牌提供它的几何定位技术的。

GeoIP可以按国家，地域位置甚至精确到城市，对互联网顾客和网站的访客进行精确实时的定位。MaxMind的GeoIP技术为在线业务提供了一个非常价值的的营销工具，并能够帮助定制优化网站以便更好地服务客户。

目前有超过2000位客户在使用GeoIP技术。MaxMind用其行业领先的minFraud服务，旨在帮助商人防止网上信用卡交易中的欺诈行为。

通过其全面的欺诈检测系统，商家可以准确地检测并自动对欺诈性质的“卡不在场交易”进行标注。我们每年检测的电子交易超过2亿笔。

目前，6000多个的电子商务企业通过我们的客户和合作伙伴关系网络共同受益于minFraud这项服务。

MaxMind的客户包括：About.com, AT&T, Dupont, Earthlink, eBay, IBM, Lexis Nexis, Lycos, Match.com, Morgan Stanley, Orbitz, Red Hat, Reed Elsevier, Sony, Walgreens, Wal-Mart, Warner Brothers, WebEx and Yahoo!. 



最近需要获取ip地址的地理位置信息（国家地区，经纬度等），就发现了maxmind。

maxmind提供了免费的可在本地部署的geo-ip数据库（GeoLite2）（mmdb以及csv格式），和geo-ip查询api服务

支持ipv4和ipv6的地理信息查询，以及ASN数据库（ip-运营商信息查询）

此前，MaxMind一直提供GeoLite2公开的访问下载地址，但从2019年12月30日开始，MaxMind不再提供GeoLite2公开的访问下载地址，需要用户注册一个MaxMind帐户并获取许可密钥，才能下载GeoLite2数据库。

每个账号每24小时只能下载2000次

Each account can perform up to 2,000 total downloads per 24 hour period.



GeoLite2数据库的下载地址即为：

```shell

# GeoLite2-Country数据库
curl -I "https://download.maxmind.com/app/geoip_download?edition_id=GeoLite2-Country&license_key=此处替换为证书密钥&suffix=tar.gz"



```


> 注意，用 curl 或 wget 下载时，要注意用双引号把 URL 引起来

https://stackoverflow.com/questions/59709494/maxmind-pulling-geolite2-gets-401-unauthorized


GeoIP数据库目前有两种格式，GeoLite（.dat文件）与 GeoLite2（.mmdb文件）。ModSecurity v2需要使用.dat格式，ModSecurity v3则使用.mmdb格式。


参考 https://www.cnblogs.com/xiaoleiel/p/8333917.html

# 更新

github actions 定期自动从 maxmind 更新geoip信息，并发布到release中
