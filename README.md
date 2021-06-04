magnet-vip
----------

本项目是一个磁力接口，可自动将磁力链接转换成种子文件提供下载，并返回磁力和磁力对应的种子的详细信息，包含文件列表信息、大小和`hashInfo`。

在线地址：https://magnet-vip.com/
 
接口使用
----

`api`请求方法，请使用`post`请求，如下：

    #接口地址
    https://api.magnet-vip.com/api2/magnetinfo
    
    #请求参数，磁力链接如magnet:?xt=urn:btih:CC8D66412F22BB03BB091049A827BABFD2D1E778
    body: {
     url: '磁力链接'
    }
    
相关信息返回：

    {
        "success": 1,
        "info": {
            "meta": {
                "createAt": "2021-06-04T15:55:49.367Z",
                "updateAt": "2021-06-04T15:55:49.367Z"
            },
            "_id": "60ba4d05a702a37cf21b9693",
            "name": "Shark Attack 2 (2000) [REPACK] [720p] [WEBRip] [YTS.MX]",
            "infoHash": "cc8d66412f22bb03bb091049a827babfd2d1e778",
            "files": [
                {
                    "_id": "60ba4d05a702a37cf21b9694",
                    "path": "Shark Attack 2 (2000) [REPACK] [720p] [WEBRip] [YTS.MX]/Shark.Attack.2.2000.REPACK.720p.WEBRip.x264.AAC-[YTS.MX].mp4",
                    "name": "Shark.Attack.2.2000.REPACK.720p.WEBRip.x264.AAC-[YTS.MX].mp4",
                    "length": 893806530
                },
                {
                    "_id": "60ba4d05a702a37cf21b9695",
                    "path": "Shark Attack 2 (2000) [REPACK] [720p] [WEBRip] [YTS.MX]/Shark.Attack.2.2000.REPACK.720p.WEBRip.x264.AAC-[YTS.MX].srt",
                    "name": "Shark.Attack.2.2000.REPACK.720p.WEBRip.x264.AAC-[YTS.MX].srt",
                    "length": 80660
                },
                {
                    "_id": "60ba4d05a702a37cf21b9696",
                    "path": "Shark Attack 2 (2000) [REPACK] [720p] [WEBRip] [YTS.MX]/www.YTS.MX.jpg",
                    "name": "www.YTS.MX.jpg",
                    "length": 53226
                },
                {
                    "_id": "60ba4d05a702a37cf21b9697",
                    "path": "Shark Attack 2 (2000) [REPACK] [720p] [WEBRip] [YTS.MX]/Subs/English.srt",
                    "name": "English.srt",
                    "length": 80660
                },
                {
                    "_id": "60ba4d05a702a37cf21b9698",
                    "path": "Shark Attack 2 (2000) [REPACK] [720p] [WEBRip] [YTS.MX]/Subs/SDH.eng.srt",
                    "name": "SDH.eng.srt",
                    "length": 85030
                }
            ],
            "category": "60b10e5a6534551065010693",
            "magnet": "magnet:?xt=urn:btih:CC8D66412F22BB03BB091049A827BABFD2D1E778",
            "length": 894106106,
            "__v": 0
        }
    }

可通过接口获取到的`infoHash`，下载种子文件，如下：

    #后面的cc8d66412f22bb03bb091049a827babfd2d1e778为获取到的infoHash信息
    https://api.magnet-vip.com/api2/download/cc8d66412f22bb03bb091049a827babfd2d1e778
