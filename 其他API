我们分析了最广泛使用的IP地理定位api的优缺点，包括:数据质量、成本、正常运行时间和其他所有你需要做决定的东西。

所有提到的服务都要花钱。不过，每一个都有一个免费层，你可以从其中一些开始，比如ipgeolocation.com, ipgeolocationapi.com和ipify.org是免费的公共设施。

ipdata的API被美国宇航局、迪士尼、康卡斯特、麦肯锡和其他数百家公司使用!注册一个免费的计划并检查我们的文档!

一、表的内容
单击以下任何一个服务跳转到它的部分。

Maxmind GeoIP2精密服务

IPData.co

IPInfo.io

IP2Location.com

DP-IP.com

IP-API.com

IPGeolocation.io

IPGeolocation.com

ipapi.co

ipstack.com

ipify.org

ipgeolocationapi.com

我们使用第三方监测工具监测每个API 24小时。我们每30秒从全球8个地点发送一次请求。洛杉矶-美国，迈阿密-美国，蒙特利尔-加拿大，Gravelines -法国，法兰克福-德国，新加坡，东京-日本，悉尼-澳大利亚。

二、Maxmind GeoIP2精密服务-检测在线欺诈和定位在线访问者

Endpoint: https://{account_id}:{license_key}@geoip.maxmind.com/geoip/v2.1/city/{ip}

API Key: Required

API Latency: 44ms

2.1 数据质量
Maxmind声称他们的GeoIP2网络服务拥有最准确的位置数据。比他们的GeoIP2数据库多定位9%的邮政编码ip和4%的美国城市ip。

Maxmind是少数几个收集自己的数据并将其发布到可下载数据库中的数据提供商之一。

2.2 数据样本
GeoIP2 web服务有3个端点;乡村、城市和见解Country, City and Insights。Insights端点提供的数据字段数量最多，精度最高，也是最贵的，每百万请求需要2000美元。

请注意，您可以以更低的每百万成本从其他提供商获得相同的数据字段，而且精确度相同或更低。

{

"city": {

  "confidence": 0,

  "geoname_id": 2151718,

  "names": {

  "en": "Research"

  }

},

"continent": {

  "code": "OC",

  "geoname_id": 6255151,

  "names": {

  "ja": "オセアニア",

  "pt-BR": "Oceania",

  "ru": "Океания",

  "zh-CN": "大洋洲",

  "de": "Ozeanien",

  "en": "Oceania",

  "es": "Oceanía",

  "fr": "Océanie"

  }

},

"country": {

  "confidence": 99,

  "iso_code": "AU",

  "geoname_id": 2077456,

  "names": {

  "zh-CN": "澳大利亚",

  "de": "Australien",

  "en": "Australia",

  "es": "Australia",

  "fr": "Australie",

  "ja": "オーストラリア",

  "pt-BR": "Austrália",

  "ru": "Австралия"

  }

},

"location": {

  "accuracy_radius": 1000,

  "latitude": -37.7,

  "longitude": 145.1833,

  "time_zone": "Australia/Melbourne"

},

"maxmind": {

  "queries_remaining": 2457

},

"postal": {

  "confidence": 0,

  "code": "3095"

},

"registered_country": {

  "iso_code": "AU",

  "geoname_id": 2077456,

  "names": {

  "en": "Australia",

  "es": "Australia",

  "fr": "Australie",

  "ja": "オーストラリア",

  "pt-BR": "Austrália",

  "ru": "Австралия",

  "zh-CN": "澳大利亚",

  "de": "Australien"

  }

},

"subdivisions": [{

  "confidence": 0,

  "iso_code": "VIC",

  "geoname_id": 2145234,

  "names": {

  "ru": "Виктория",

  "en": "Victoria",

  "pt-BR": "Vitória"

  }

}],

"traits": {

  "user_type": "content_delivery_network",

  "autonomous_system_number": 13335,

  "autonomous_system_organization": "Cloudflare Inc",

  "isp": "APNIC and Cloudflare DNS Resolver project",

  "organization": "APNIC and Cloudflare DNS Resolver project",

  "ip_address": "1.1.1.1"

}

}

2.3基础设施
GeoIP2 web服务由Softlayer in托管的4个端点提供;

维吉尼亚州(美国)

圣何塞，加利福尼亚(美国)

伦敦(英国)

新加坡

Maxmind使用基于延迟的路由将你的请求发送到他们认为离你最近的区域，这样你的请求就能以最低的延迟得到服务。

然而，他们的自动路由是不确定的，在测试一个来自非洲服务器的呼叫时，我的请求是由他们的一个美国端点处理的，而我希望被路由到他们的英国端点。

同时，在他们的端点上运行dig会返回一个单一的a记录，这意味着他们正在终止一个服务器上的所有请求。这可能不是最有效的设置。

更新:
Maxmind现在使用Cloudflare作为CDN，这将大大提高其正常运行时间和全球响应时间

成本
对于通过city终端进行的基本城市级别的地理定位，每百万次呼叫需要支付400美元，每请求支付0.0004美元。

Insights终端每请求花费0.002美元，每百万次通话花费2000美元。

他们在定价页面上提到，每月超过2500美元的销量有折扣。

开始
Maxmind有很好的文档和针对多种语言的库。

API使用基本授权，因此需要HTTPs，以安全地传输登录细节。

在这里注册一个免费试用账户，你将获得5美元的积分，足够支付12500个City终端请求。

然后尝试;

curl -u “{account_id}:{license_key}” \ “https://geoip.maxmind.com/geoip/v2.1/insights/me?pretty"

和

curl -u “{account_id}:{license_key}” \

“https://geoip.maxmind.com/geoip/v2.1/insights/{ip_address}?pretty"

三、IPData.co快速地理定位与可靠的性能



Endpoint: https://api.ipdata.co?api-key=test

API Key: Required

API Latency: 65ms




数据样本
IPData API提供;

IP地址位置数据 IP Address Location Data-国家，地区，城市，长/长，邮政编码，ISP和组织

运营商检测Carrier Detection -我们将返回运营商的品牌名称，例如Verizon, T-Mobile，他们的移动国家代码和移动网络代码

Tor检测Tor Detection ——我们返回一个标志，告诉您一个IP地址是否是Tor退出节点

代理检测Proxy Detection——我们聚合多个列表，跟踪打开的代理，并返回一个标志，告诉您一个IP地址是否为代理

威胁数据Threat Data-检查一个IP地址最近是否被报告为恶意活动的来源

货币数据Currency Data- IP地址所属国家的主要货币。包括符号、代码和名称。

时区数据Timezone Data—IP地址所在地区的时区

语言数据anguage Data - IP地址所在国家的主要语言

欧盟探测EU Detection-是否一个IP地址属于欧盟的一个国家

ASN检测ASN Detection- IP所属的ASN组织以及该组织的使用类型如。“主机”、“isp”、“教育”等，“hosting”, “isp”, “education”

{

  "ip": "1.1.1.1",

  "is_eu": false,

  "city": "Research",

  "region": "Victoria",

  "region_code": "VIC",

  "country_name": "Australia",

  "country_code": "AU",

  "continent_name": "Oceania",

  "continent_code": "OC",

  "latitude": -37.7,

  "longitude": 145.1833,

  "asn": "AS13335",

  "organisation": "Cloudflare Inc",

  "postal": "3095",

  "calling_code": "61",

  "flag": "https://ipdata.co/flags/au.png",

  "emoji_flag": "🇦🇺",

  "emoji_unicode": "U+1F1E6 U+1F1FA",

  "asn": {

        "asn": "AS13335",

        "name": "Cloudflare, Inc.",

        "domain": "cloudflare.com",

        "route": "1.1.1.0/24",

        "type": "hosting"

  },

  "languages": [

    {

      "name": "English",

      "native": "English"

    }

  ],

  "currency": {

    "name": "Australian Dollar",

    "code": "AUD",

    "symbol": "AU$",

    "native": "$",

    "plural": "Australian dollars"

  },

  "time_zone": {

    "name": "Australia/Melbourne",

    "abbr": "AEST",

    "offset": "+1000",

    "is_dst": false,

    "current_time": "2018-07-05T05:22:19.138894+10:00"

  },

  "threat": {

    "is_tor": false,

    "is_proxy": false,

    "is_anonymous": false,

    "is_known_attacker": false,

    "is_known_abuser": false,

    "is_threat": false,

    "is_bogon": false

  }

}

以上所有数据在免费和付费计划中都是可用的。

ASN数据样本
"asn": "AS13335",

    "name": "Cloudflare, Inc.",

    "domain": "cloudflare.com",

    "route": "1.1.1.0/24",

    "type": "hosting"

}

运营商数据样本
{

"name": "T-Mobile",

"mcc": "310",

"mnc": "160"

}

威胁数据样本
{

“is_tor”: true,

“is_proxy”: false,

“is_anonymous”: true,

“is_known_attacker”: false,

“is_known_abuser”: true,

“is_threat”: true,

“is_bogon”: false

}

为了测试威胁数据，从Tor出口节点列表中随机挑选IP地址，is_tor和is_anonymous将为真。https://check.torproject.org/torbulkexitlist?ip=1.1.1.1

Tor出口节点也经常被恶意用户使用，您可能还会看到一些ip将返回is_known_abuser和is_known_攻击者为true。

有关详细信息，请参见威胁数据文档。

基础设施
IPData提供了运行在Amazon全球基础设施上的高可用API。

在高可扩展性博客和AWS创业博客上了解我们的基础设施。API在全球有11个端点提供服务，其中4个在美国，1个在加拿大。

维吉尼亚州(美国)

俄亥俄州(美国)

北加利福尼亚(美国)

俄勒冈州(美国)

加拿大

法兰克福(德国)

伦敦(英国)

首尔(韩国)

悉尼(澳大利亚)

孟买(印度)

圣保罗(巴西)

我们使用AWS Route53基于延迟的路由，从离您最近的区域为您的请求提供服务。

对API端点的挖掘将从离你最近的端点返回2条随机的A记录。每个APIGateway端点都是无限可伸缩的，每秒能够处理10,000多个请求!

通过我的笔记本电脑进行测试，我的大部分请求被发送到孟买，其余的被发送到法兰克福。这是有道理的，因为那些数据中心在地理上离我最近。

成本

我们最小的计划是每月10美元，每天2500个请求或每月7.5万个请求。我们最大的计划是每月120美元，每天10万或每月300万的请求。

我们的企业定价从每天1,000,000个或更多的请求开始，每百万次调用20美元。

有4个定价层次;


基本-每天2500个请求或每月7.5万个请求，费用为10美元

Lite -每天10,000个请求或每月300,000个请求，收费30美元

创业——每天5万次或每月150万次，收费50美元

业务——每天100,000个请求或每月3,000,000个请求，价格为120美元

我们每百万人的成本很低，我们把节省下来的成本转嫁给用户。

所有套餐年费八折。

请访问sales@ipdata.co了解企业定价。

域和IP地址白名单
您可以选择将API密钥的使用限制为域或IP地址列表。要为您的API密钥启用此功能，请发送一封电子邮件到support@ipdata.co

批量查询
您可以在一个API调用中查找多达100个IP地址!这与ipdata API的一般速度相结合，意味着您可以非常快速地定位数百万个IP地址。更多信息见文档。

开始
我们在这里提供了非常简单的文档，其中有多种语言的示例，以及社区提供的许多特定于语言的库。


API仅通过HTTPs提供，并通过API密钥作为一个名为“API -key”的查询字符串参数或同名的头来处理身份验证。

在这里注册一个免费的API密钥。免费层允许每天1500个请求或每月45,000个请求。

例子;

获取呼叫ip地址的数据

curl https://api.ipdata.co?api-key=test

查找指定的ip地址

curl https://api.ipdata.co/1.1.1.1?api-key=test

您还可以选择一个特定的字段，例如仅选择country_name

curl https://api.ipdata.co/1.1.1.1/country_name?api-key=test

或者is_eu字段

curl https://api.ipdata.co/1.1.1.1/is_eu?api-key=test

为IPv6

curl https://api.ipdata.co/2601:8: be00: cf20: ca60: ff: fe09:35b5 ? api key =测试

四、IPInfo.io地理位置和数据解决方案

Endpoint: https://ipinfo.io/json

API Key: Not Required

API Latency: 165ms




数据样本
IPInfo.io API返回他们的免费层和最便宜的计划上的基本地理位置数据。

每一个连续的定价层都有更多的数据。

基本计划-提供基本的地理位置和ASN详细信息

Standard Plan - Basic加上ASN类型，即ASN是业务、主机还是ISP。您还可以通过ASN进行查找并获得优先级支持。

专业计划-标准的一切加上公司和承运人的细节。您还可以获得IP类型，即IP地址是否属于企业、主机提供商或ISP。

API还返回与IP地址相关联的主机名。

{

"ip": "1.1.1.1",

"hostname": "1dot1dot1dot1.cloudflare-dns.com",

"city": "Research",

"region": "Victoria",

"country": "AU",

"loc": "-37.7000,145.1830",

"postal": "3095",

"org": "AS13335 Cloudflare, Inc."

}

这是免费API提供的数据。

他们公司的数据是这样的;

{

“ip”: “38.104.128.99”,

“name”: “American Heart Association”,

“domain”: “americanheart.org”

}

Carrier的数据是这样的;

{

“ip”: “201.144.87.19”,

“carrier”: “Telcel”,

“country”: “MX”,

“mcc”: “334”,

“mnc”: “20”

}

基础设施
IPInfo有3个端点运行在谷歌Cloud in;

加州

伦敦

法兰克福

你可以阅读IPInfo.Io的基础设施。

在ipinfoio端点上运行dig将返回4条属于谷歌的A记录。显示具有负载平衡的高可用设置。IPInfo还使用基于延迟的路由服务于离你最近的端点的请求。

他们的路由似乎也将我的所有请求路由到加州的服务器，而我希望我的请求从他们的欧洲端点得到服务。

成本

我们之前提到过IPInfo的3个计划，但没有定价和数量。记住，每一层都有额外的数据。

在这里;

基本计划-每月25万次请求，每月49美元订阅

标准计划-每月200万的请求，每月249美元的订阅

Pro计划-每月600万请求999美元每月订阅

他们对每月超过600万次的通话量有定制定价。

如果你订阅年费，你可以得到两个月的免费或16%的折扣。

开始
向ipinfo API发出请求不需要API密钥。

文档主要是CLI示例。这里有一些指向特定语言库的链接。

在这里注册一个免费的API密钥。

获取自己的ip信息

curl ipinfo.io

查找指定的ip地址

curl ipinfo.io / 8.8.8.8

验证示例;

使用基本认证

-u {api-key}: ipinfo.io

使用承载令牌

curl -H ‘Authorization: Bearer {api-key}’ ipinfo.io

使用令牌查询参数

curl ipinfo.io?token={api-key}

五、IP2Location.com -通过IP地址识别地理位置


Endpoint: https://api.ip2location.com/v2/?ip=1.1.1.1&key={YOUR_API_KEY}&package=WS24&addon=continent,country,region,city,geotargeting,country_groupings,time_zone_info"

API Key: Required

Demo: https://www.ip2location.com/demo

HTTPS Support: Yes

介绍
IP2Location是互联网上最古老的IP地理定位服务之一，已经存在了18多年。他们发布了大约24个IP地理位置数据库，并提供了一些代理检测数据库。

这是一个Geolocation API响应的示例;

{

  "country_code":"HK",

  "country_name":"Hong Kong",

  "region_name":"Hong Kong",

  "city_name":"Hong Kong",

  "latitude":"22.28552",

  "longitude":"114.15769",

  "zip_code":"-",

  "time_zone":"+08:00",

  "isp":"APNIC and CloudFlare DNS Resolver Project",

  "domain":"cloudflare.com",

  "net_speed":"T1",

  "idd_code":"852",

  "area_code":"02522",

  "weather_station_code":"CHXX0049",

  "weather_station_name":"Hong Kong",

  "mcc":"-",

  "mnc":"-",

  "mobile_brand":"-",

  "elevation":"4",

  "usage_type":"CDN",

  "credits_consumed":33,

  "continent":{

      "name":"Asia",

      "code":"AS",

      "hemisphere":[

        "north",

        "east"

      ],

      "translations":[]

  },

  "country":{

      "name":"Hong Kong",

      "alpha3_code":"HKG",

      "numeric_code":"344",

      "demonym":"Hong Kongese",

      "flag":"https:\/\/cdn.ip2location.com\/assets\/img\/flags\/hk.png",

      "capital":"-",

      "total_area":"1104",

      "population":"7428887",

      "currency":{

        "code":"HKD",

        "name":"Hong Kong Dollar",

        "symbol":"$"

      },

      "language":{

        "code":"ZH",

        "name":"Chinese"

      },

      "idd_code":"852",

      "tld":"hk",

      "translations":[]

  },

  "region":{

      "name":"Hong Kong",

      "code":"HK",

      "translations":[]

  },

  "city":{

      "name":"Hong Kong",

      "translations":[]

  },

  "geotargeting":{

      "metro":"-"

  },

  "country_groupings":[

      {

        "acronym":"APAC",

        "name":"Asia-Pacific"

      },

      {

        "acronym":"APEC",

        "name":"Asia-Pacific Economic Cooperation"

      },

      {

        "acronym":"Four Asian Tigers",

        "name":"Four Asian Tigers"

      },

      {

        "acronym":"Greater China",

        "name":"Greater China"

      }

  ],

  "time_zone_info":{

      "olson":"Asia\/Hong_Kong",

      "current_time":"2020-01-29T22:03:51+08:00",

      "gmt_offset":28800,

      "is_dst":"no"

  }

}}

基础设施
IP2Location在AWS的Cloudfront CDN上运行他们的服务。

成本
它们的API价格可以在这里找到。

他们在以下等级出售积分而不是订阅;

a. WS -每年10万学分49美元

b. WS10X -每年100万学分441美元

c. WS50X -每年500万信用额1960美元

注意，一个请求不一定转化为一个学分。查找IP地址所在的国家和城市需要2个积分。获取国家、地区、城市、经纬度需要5个积分。更多信息请点击这里。

开始
你需要在这里注册一个免费的API密钥，它应该允许你访问他们的免费下载数据库。

运行命令查找IP地址1.1.1.1

curl https://api.ip2location.com/v2/?ip=1.1.1.1&key={YOUR_API_KEY}&package=WS24&addon=continent,country,region,city,geotargeting,country_groupings,time_zone_info"

六、IP- api.com - IP地理定位API



Endpoint: http://ip-api.com

API Key: Not Required

API Latency: 97ms

HTTPS Support: Only on Pro




数据样本
IP-API.com只返回地理位置数据，没有其他提供商提供的丰富数据。然而，他们是唯一提供3个月45欧元无限制计划的供应商。此外，它们也是少数支持XML和CSV的提供商之一。

这个API是无限的，只要你一分钟发出的请求少于150个或者每秒2个请求。

从我所做的测试来看，API似乎稳定而快速，每天可以服务数亿个调用。

基础设施
我找不到ip-api.com的服务器列表。然而，从运行几个服务器的测试，我能够找到端点;

罗马尼亚

德国

密苏里州(美国)

在ip-api.com端点上运行dig会从离你最近的端点返回2条A记录。

它们基于延迟的路由似乎工作得很好，我的请求是从罗马尼亚和德国提供的。从美国的服务器进行测试，请求是在美国境内服务的。

我希望世界上有更多的端点，以便API能够提供我在测试中发现的那种始终如一的高性能。

成本
ip-api.com的专业版提供了3个计划，所有计划都有无限的请求。

3个月的访问费用为45欧元

6个月的访问费用为85欧元

12个月的访问费用为每月160欧元或13欧元

开始
你可以在这里注册一个付费计划。然而，开始使用服务并不需要API密钥。

注意，自由层只允许通过普通HTTP请求。免费层也不允许商业使用。

查找您自己的ip数据

curl http://ip-api.com/json

查找特定的ip地址

curl http://ip-api.com/json/1.1.1.1

{"status":"success","country":"Australia","countryCode":"AU","region":"QLD","regionName":"Queensland","city":"South Brisbane","zip":"4101","lat":-27.4766,"lon":153.0166,"timezone":"Australia/Brisbane","isp":"Cloudflare, Inc","org":"APNIC and Cloudflare DNS Resolver project","as":"AS13335 Cloudflare, Inc.","query":"1.1.1.1"}

七、ipgeolocation.io -免费IP地理位置API和IP位置查找数据库



Endpoint: https://api.ipgeolocation.io/ipgeo

API Key: Required

API Latency: 51ms

HTTPS Support: Yes




数据样本
ipgeolocation.io为您提供当前的时间，日期，年，时区和地理位置信息，从时区，lat/lang，国家，城市或IP地址信息。

它同时支持JSON和XML。除了IP地理定位API之外，他们还有两个有趣的互补API。一个时区API和一个天文API。

这是他们API响应的样本;

{

    "ip": "8.8.8.8",

    "hostname": "google-public-dns-a.google.com",

    "continent_code": "NA",

    "continent_name": "North America",

    "country_code2": "US",

    "country_code3": "USA",

    "country_name": "United States",

    "country_capital": "Washington",

    "state_prov": "California",

    "district": "",

    "city": "Mountain View",

    "zipcode": "94043",

    "latitude": "37.4229",

    "longitude": "-122.085",

    "is_eu": false,

    "calling_code": "+1",

    "country_tld": ".us",

    "languages": "en-US,es-US,haw,fr",

    "country_flag": "https://ipgeolocation.io/static/flags/us_64.png",

    "isp": "Level 3 Communications",

    "connection_type": "",

    "organization": "Google Inc.",

    "geoname_id": "5375480",

    "currency": {

        "code": "USD",

        "name": "US Dollar",

        "symbol": "$"

    },

    "time_zone": {

        "name": "America/Los_Angeles",

        "offset": -8,

        "current_time": "2019-01-14 03:30:00.135-0800",

        "current_time_unix": 1547465400.135,

        "is_dst": false,

        "dst_savings": 1

    }

}

基础设施
ipgeolocation使用Cloudflare CDN，这意味着他们的全球延迟很好。

成本
专业版的ipgeolocation.IO有以下层次;

铜-每月15万请求15美元

银-每月100万的请求65美元

银+ -每月300万要求130美元

黄金-每月600万请求200美元

铂金:每月2000万请求500美元

开始
你需要在这里注册一个免费的API密钥，它允许你每天1000个请求。

运行命令查找IP地址1.1.1.1

curl 'https://api.ipgeolocation.io/ipgeo?apiKey=API_KEY&ip=1.1.1.1'

查询IPv6地址

curl 'https://api.ipgeolocation.io/ipgeo?apiKey=API_KEY&ip=2001:4860:4860::1'

八、ipgeolocation.com



Endpoint: ipgeolocation.com

API Key: Not Required

API Latency: 30ms

数据样本
ipgeolocation.com是一个免费的IP地理定位API工具。它返回城市级别的地理位置以及AS编号和组织。

{

“ip”: “138.68.161.60”,

“city”: “London”,

“region”: “England”,

“country”: “United Kingdom”,

“coords”: “51.535300,-0.665800”,

“asn”: “AS14061, DigitalOcean, LLC”,

“postal”: “SL1”,

“timezone”: “Europe/London”

}

开始
查找您自己的IP地址

curl ipgeolocation.com

查找特定的ip地址

curl ipgeolocation.com/1.1.1.1

强制JSON响应

curl ipgeolocation.com ? json = 1

九、ipapi.co



Endpoint: https://ipapi.co/json

API Key: Not Required

API Latency: 270ms




数据样本

ipapi.co返回基本的地理位置数据和货币、时区、语言和UTC偏移量的单个字段。

{

"ip": "1.1.1.1",

"city": "Research",

"region": "Victoria",

"region_code": "VIC",

"country": "AU",

"country_name": "Australia",

"continent_code": "OC",

"in_eu": false,

"postal": "3095",

"latitude": -37.7,

"longitude": 145.1833,

"timezone": "Australia/Melbourne",

"utc_offset": "+1000",

"country_calling_code": "+61",

"currency": "AUD",

"languages": "en-AU",

"asn": "AS13335",

"org": "Cloudflare Inc"

}


基础设施
关于ipapi.co的基础设施，除了它是自动伸缩的事实外，并没有太多的文档。

在ipapi.co端点上运行dig时，会返回两个A记录，但这两个记录都属于Cloudflare，这意味着请求在路由到其后端之前要经过Cloudflare的边缘位置。

这就解释了api的低apdex。从向上向下的数据来看，大多数请求(861)在500毫秒内得到服务，只有178个请求在125毫秒以下得到服务

成本
免费1000个请求一天

每天2000个请求，每月15美元

每天5000个请求，每月25美元

每天15000个请求，每月49美元

每天5万次请求，每月99美元

每天200,000个请求，每月199美元

每天50万，每月399美元

对于年度注册也有20%的折扣。

开始
你不需要注册才能使用ipapi.co API。

这里记录了API

十、ipstack.com



Endpoint: http://api.ipstack.com

API Key: Required

API Latency: 144ms


数据样本
IPStack.com为您提供更大计划的更多数据。他们目前有4个计划;

免费-仅地理位置数据。没有SSL支持。不允许商业用途。

基本- SSL支持。位置、货币、时区和连接数据。

专业-所有的基本和访问批量查找端点。

专业加-专业加的一切访问安全数据，包括;代理，爬虫和tor检测。

他们的免费计划只返回地理位置数据。像下面;

{

"ip": "134.201.250.155",

"type": "ipv4",

"continent_code": "NA",

"continent_name": "North America",

"country_code": "US",

"country_name": "United States",

"region_code": "CA",

"region_name": "California",

"city": "Huntington Beach",

"zip": "92648",

"latitude": 33.6746,

"longitude": -118.0086,

"location": {

  "geoname_id": 5358705,

  "capital": "Washington D.C.",

  "languages": [{

  "code": "en",

  "name": "English",

  "native": "English"

  }],

  "country_flag": "http:\/\/assets.ipstack.com\/flags\/us.svg",

  "country_flag_emoji": "\ud83c\uddfa\ud83c\uddf8",

  "country_flag_emoji_unicode": "U+1F1FA U+1F1F8",

  "calling_code": "1",

  "is_eu": false

}

}

基础设施
IPStack目前只有一个终端在圣何塞(美国)由Softlayer托管。

在api.ipstack.com端点上运行dig返回一个apilayer.net的CNAME记录。Apilayer是ipstack.com和其他一些api的开发公司。

再次在apilayer.net上运行dig，返回2个服务器的2个A记录，一个在达拉斯(美国)，另一个在圣何塞(美国)。这意味着美国海岸和欧洲的用户将会经历较高的延迟。

成本



基本-每月50000个请求，10美元

专业-每月50万份申请，50美元

职业加-每月有200万份申请，要求100美元

每年打八折。

开始
在这里查看ipstack的文档。

你可以在这里注册一个API密钥。你需要注册免费层。

然后查找自己的ip地址数据

curl http://api.ipstack.com/check?access_key= {api密匙}

或查找任何其他ip地址

curl http://api.ipstack.com/134.201.250.155?access_key= {api密匙}

十一、db-ip.com



Endpoint: https://api.db-ip.com/v2/{api-key}/1.1.1.1

API Key: Required

API Latency: 225ms




数据样本
Db-ip.com是这个列表中唯一提供他们的数据的可下载版本的提供商。

{

    "ipAddress": "1.1.1.1",

    "continentCode": "OC",

    "continentName": "Oceania",

    "countryCode": "AU",

    "countryName": "Australia",

    "stateProv": "Queensland",

    "city": "South Brisbane"

}

基础架构
他们的网站提到，他们使用Anycast来确保您的请求从离您最近的端点得到服务。他们还提到他们的基础设施是全局的，但是我没有在他们的站点上找到端点列表。

成本



新手-每天50000个请求，15.90欧元

保险费-每天100万请求99.90欧元

企业-无限请求499.90

开始
他们的文档看起来很简单，但是例子都是PHP和Javascript的。

您需要一个API密钥来访问它们的自由层。自由层每天允许1000个请求，不能通过HTTPS访问，返回文档中提到的有限数据

十二、ipgeolocationapi.com



Endpoint: https://api.ipgeolocationapi.com/geolocate/91.213.103.0

API Key: No

API Latency: 50ms

开始
ipgeolocationapi.com是一个有趣的开源项目，似乎只在Cloudflare的员工中运行，并使用Cloudflare的地理定位头文件。

因此，它的响应速度非常快，不到80ms。然而，它似乎只拥有国家一级的数据，而没有将ip定位到城市一级。

和!你可以在他们的API文档中部署你自己的托管ip地址API和他们的Heroku按钮!

十三、通过ipify.org获得你的公共IP地址
如果你所需要的只是一个简单的Javascript API IP查找API，那么我们推荐ipify.org。

Randall Degges是ipify.org的创建者，他写了一个非常有趣的故事，讲述了ipify.org是如何开始并发展到每月在Heroku上服务300亿个调用的。

你可以在他的博客上读到一篇文章——《到300亿人及以上》。

Ipify的使用是免费的，没有限制，并引用他们的主页“即使你正在做数百万的请求每分钟”!

例子

curl 'https://api.ipify.org'

或者获取JSON格式的响应

curl 'https://api.ipify.org?format=json'

