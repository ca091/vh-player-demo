# vh-player

> 创建实例

```javascript
let options = {
  videoNode: 'vh-player',
  type: 'vod',
  autoplay: true,
  controls: 'custom',
  muted: false,
  // poster: 'http://www.vhallyun.com/img/index-banner2.7b949168.png'
  debug: true,
  flvOptions: {
    enableWorker: false,
    statisticsInfoReportInterval: 3000, // 信息上报间隔
  },
  hlsOptions: {
    debug: false,
    levelLoadingMaxRetry: -1, // todo 自己做重连，不使用hls自带重连
  },
  type: type || 'vod',
  appId: qs.appId, // 'N5oMU37i' : 'UNUBw1EB'
  accountId: 405,
  token: 'vhall',
  liveOption: {
    roomId: qs.roomId, // 'lss_jZqjePJY' : 'lss_XeTu8XDD'
    type: (qs.playerType as PlayerTypes) || PlayerTypes.Flv
  },
  vodOption: {
    recordId: qs.recordId // 58faa1f6
  },
  scheduleOption: {
    enable: qs.schedule === 'true',
    playerData: type === 'live' ? liveData : vodData,
    debugUrl: qs.url ? qs.url + (qs.url.indexOf('?token') !== -1 ? '' : '?token=alibaba') : '',
    debugCDN: (qs.cdn as CDNNames) || CDNNames.TX,
    debugPlayer: qs.playerType as PlayerTypes
  },
  peer5Option: {
    enable: qs.peer5 === 'true',
    customerId: qs.peer5CustomerId,
    fallback: true
  },
  switchOption: {
    enable: true
  },
  pursueOption: {
    enable: true
  },
  marqueeOption: {
    enable: true,
    type: 1,
    text: 'test marquee'
  },
  vttOptions: {
    enable: true,
    tracks: [
      {label: '英文', kind: 'subtitles', srclang: 'en', src: location.pathname + 'vtt/subtitles_en.vtt'},
      {label: '中文', kind: 'subtitles', srclang: 'zh', src: location.pathname + 'vtt/subtitles_zh.vtt', default: true},
    ]
  },
  uiOptions: {
    line: {
      [CDNNames.TX]: '腾讯线路',
      [CDNNames.ALI]: '备用线路1',
      [CDNNames.HW]: '备用线路2',
      [CDNNames.CY]: '备用线路3',
    },
    quality: {
      [Quality.PSame]: '原画',
      [Quality.P720]: '高清',
      [Quality.P480]: '标清',
      [Quality.P360]: '流畅',
      [Quality.Pa]: '音频',
    }
  }
}
```
