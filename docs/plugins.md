## barrage 弹幕

- method
  - addBarrage(content: string, style = {}): void
  - clearBarrage(): void
  - openBarrage(): void
  - closeBarrage(): void

## capture 截图

- method
  - capture(): string

## fullscreen 全屏

- prop
  - isFullscreen: boolean
- method
  - enterFullscreen: () => Promise<any>
  - exitFullscreen: () => Promise<any>
  - toggleFullscreen: () => Promise<any>
- event
  - FULLSCREEN_CHANGED (boolean)

## lag 卡顿检测

- event
  - LAG_REPORT {times, beginTime} => {卡顿次数, 开始卡顿时间}
  - LAG_RECOVER {lastTime} => {卡顿持续时间}

## marquee 跑马灯

## pursue 追播

## replay 暂停恢复

## schedule 调度

- method
  - setQuality(quality: Quality): void

## switcher 切线

- method
  - switch(line?: string): void
  - openLiveSubtitle(): void ⌛️
  - closeLiveSubtitle(): void ⌛️

## timeshift 直播时移

- method
  - handleTimeShift(delay: number = 0): void
- event
  - LIVE_TIMESHIFT {delay, url}

## UI 控制栏皮肤

- method
  - openUI(): void
  - hideUI(): void

## vtt 回放字幕

- method
  - selectVtt(srclang: string): void
  - closeVtt(): void
