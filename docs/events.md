## video 事件

- Error = 'error',
- Waiting = 'waiting',
- Ended = 'ended',
- Loaded = 'loadeddata',
- Play = 'play',
- Canplay = 'canplay',
- Pause = 'pause',

- Ratechange = 'ratechange',
- Stalled = 'stalled',
- Volumechange = 'volumechange',

## 自定义事件

- VTT_ADDED = 'vttAdded',
- VTT_SELECTED = 'vttSelected',
- VTT_CLOSED = 'vttClosed',
- DEFINITION_CHANGE = 'definitionChange', // 执行切换清晰度
- LIVESUBTITLE_OPENED = 'liveSubtitleOpened', // 直播字幕开启事件
- LIVESUBTITLE_CLOSED = 'liveSubtitleClosed', // 直播字幕关闭事件
- AUTOPLAY_FAILED = 'autoplayFailed', // 自动播放失败事件

- FULLSCREEN_CHANGED = 'fullscreenChanged', // 全屏状态改变
- LAG_REPORT = 'lagReport', // 卡顿
- LAG_RECOVER = 'lagRecover', // 卡顿恢复
- OPEN_BARRAGE = 'openBarrage', // 开启弹幕
- CLOSE_BARRAGE = 'closeBarrage', // 关闭弹幕
- CLEAR_BARRAGE = 'clearBarrage', // 清空弹幕

- SCHEDULER_COMPLETE = 'scheduleComplete',

- PULL_STREAM_FAILED = 'PULL_STREAM_FAILED', // 拉流失败 - 执行重连
- LINE_CHANGE = 'lineChange', // 执行切线
- LINE_CHANGED = 'lineChanged', // 切线完成，包含切换清晰度
- LIVE_TIMESHIFT = 'liveTimeShift', // 直播时移事件
- TOUCH_PLAY = 'touchPlay', // 触发播放, 用于日志上报

- HLS_ERROR = 'hlsError', // HLS错误
- FLV_ERROR = 'flvError' // HLS错误
