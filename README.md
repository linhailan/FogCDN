# FogVDN - The Video CDN in the Fog with Crowdsourcing

  Pear（梨享）出品的一个面向未来、专注于服务在线视频流媒体的CDN。它是Pear Fog（梨享雾计算）平台的重要组成部分，具有以下特色：

## <img src="fig/icon/一键接入.png" width="24"> 集成方便，CP或CDN均可“一键启用”

``` js
<video id="v1" src="https://example.com/v1.mp4"></video>
<script src="PearPlayer.js"></script>
<script>
    var PearPlayer = require('PearPlayer');
    PearPlayer('#v1',{
        type: 'mp4',
        token: token
    });
</script>
```

> FogVDN是Web友好的，使用开放的Web标准（不需要额外的任何插件，只需要HTML5和WebRTC）
> 非常容易集成到现有项目中，只需几行JS代码便可以集成

## <img src="fig/icon/延迟.png" width="24"> 超低延迟 

## <img src="fig/icon/海量规模.png" width="24"> 众包，海量节点，广覆盖

   - 拥有海量可持续稳定提供服务的节点。
   - 大部分带宽、存储、计算资源通过众包方式收集自终端用户稳定在线的边缘设备。
   - 服务能力覆盖全部地域、所有运营商、每处网络边缘。
   - 动态、实时的感知和调度，让数据传输距离尽可能接近“零跳”。

![节点架构](fig/pear-fog-node-engine.png)

## <img src="fig/icon/iso.png" width="24"> 支持开放的、国际标准的协议，如：

   + [HTTP2](https://en.wikipedia.org/wiki/HTTP/2)
   + [WebRTC](https://webrtc.org/)
   + [HLS](https://developer.apple.com/streaming/)
   + [DASH](http://mpeg.chiariglione.org/standards/mpeg-dash)
  
## <img src="fig/icon/连接一切.png" width="24"> Web友好，“连接一切”

![播放器](fig/PearPlayer.png)

## <img src="fig/icon/智能算法.png" width="24"> 高效率，在VoD、Live、VoIP等场景中均有专门优化的定制算法

## <img src="fig/icon/ssl_ca.png" width="24"> 安全可靠

   支持整个传输链路的安全传输，防止文件被篡改,避免版权文件的泄漏及内容劫持等。
   
   
   * 所有边缘节点支持TLS，HTTP默认使用HTTPS(HTTP2.0)通道
   * WebRTC通道传输数据使用SCTP协议和DTLS加密来保护
   * 信令通信是通过安全的WebSocket完成的，该WebSocket也使用TLS/SSL加密

## <img src="fig/icon/核心技术.png" width="24"> 核心技术

   Pear FogVDN目前拥有完全自主研发多项核心技术

<img src="fig/icon/延迟.png" width="24">   独立研发的分布式CDN通过共享经济的模式改变了传统CDN的技术结构，通过海量的节点，让数据传输距离可近至1km。
<br>
<br>
<img src="fig/icon/安全.png" width="24">   在数据传输上，传统CDN是一对多的，即用户平均服务质量和用户数呈“逆线性关系”。Pear FogVDN采取从多源多通道获取文件数据的方案，减少了对单点和单链路的依赖，解决了播发高清视频而单链路无法满足此带宽出现的卡顿问题，通过UDP通道也解决弱网环境丢包的问题，让用户获得更佳的下载体验。
<br>
<br>

  ![multisources](fig/fogvdn_multisources.png)
  
<img src="fig/icon/安全.png" width="24">   在数据安全方面，支持整个传输链路的安全传输。
<br>
<br>

## <img src="fig/icon/降低成本.png" width="24">  低成本

   相对于传统CDN依赖于昂贵的机房、服务器和租赁带宽，Pear FogVDN凭借海量的节点共享经济的模式，价格可低至传统CDN的一半。


## 智能内容分发和调度

   1. 高效分发网络
   
      * 精确、实时感知数据热度，把内容快速Push到边缘节点。

   2. 精确解析
   
      * 99.999%地识别访问用户的真实IP地址（及时在使用VPN的情况下），并99.9%地映射到所处区域、ISP，筛选出距离近乎“零跳”的节点为用户提供优质服务。

   3. 智能调度和切换
   
      * 即使是服务的时候，也会动态探测其他节点的健康状态和服务能力，自动切换到最优的节点组并实时调整数据比例，保障用户观看体验。
