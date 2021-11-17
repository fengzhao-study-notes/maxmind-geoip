# maxmind-geoip

https://blog.maxmind.com/2019/12/18/significant-changes-to-accessing-and-using-geolite2-databases/

# License

This repository includes [GeoLite2](https://dev.maxmind.com/geoip/geoip2/geolite2/) data created by [MaxMind](https://www.maxmind.com).


# GEOIP简介

Geo是geographic的缩写，意思是地理的，GeoIP即为IP地理位置数据库，可以根据IP获得地理位置信息。

GeoLite2是GeoIP2的免费版本，与GeoIP2数据库相比准确性较差。GeoLite2数据库每周更新国家、城市和自治系统编号信息，更新时间为每周二。

IP地理定位本质上是不精确的，地点通常靠近人口中心。GeoIP数据库提供的任何位置不应用于识别特定地址或家庭，使用精度半径作为IP地址返回的纬度和经度坐标的地理定位精度指示，IP地址的实际位置可能在这个半径和经纬度坐标所定义的区域内。




# Maxmind GEOIP简介

最近需要获取ip地址的地理位置信息（国家地区，经纬度等），就发现了maxmind。

maxmind提供了免费的可在本地部署的geo-ip数据库（GeoLite2）（mmdb以及csv格式），和geo-ip查询api服务

支持ipv4和ipv6的地理信息查询，以及ASN数据库（ip-运营商信息查询）

此前，MaxMind一直提供GeoLite2公开的访问下载地址，但从2019年12月30日开始，MaxMind不再提供GeoLite2公开的访问下载地址，需要用户注册一个MaxMind帐户并获取许可密钥，才能下载GeoLite2数据库。

GeoLite2数据库的下载地址即为：https://download.maxmind.com/app/geoip_download?edition_id=GeoLite2-Country&license_key=此处替换为证书密钥&suffix=tar.gz




# 更新

github actions 定期自动从 maxmind 更新geoip信息，并发布到release中
