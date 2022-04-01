```typescript
type LiveOption = {
  roomId: string
  type?: PlayerTypes | 'auto'
  defaultDefinition?: Quality
}

type VodOption = {
  recordId: string
  defaultDefinition?: Quality
}

// 弹幕插件
export type BarrageOptions = {
  enable: boolean
  positionRange: number[]
  speed: number // 速度固定，运动时长可变
  style?: Record<string, any>
  defaultOpen?: boolean
}

// 跑马灯插件
export type MarqueeOptions = {
  enable: boolean
  text?: string
  type?: number // 0平滑，1闪动
  position?: number // 1随机，2上，3中，4下
  interval?: number // 滚动间隔 单位秒
  duration?: number // 滚动时长
  alpha?: number
  fontSize?: number
  fontColor?: string
  height?: number
}

// 水印插件
export type WatermarkOptions = {
  enable: boolean
  alpha?: number
}

export type PursueConfig = {
  bufferPursue: number // 达到最大缓冲时间 启动追播 - 倍速播放
  bufferSeek: number // 达到最大缓冲时间 启动追播 - 跳播
  bufferStop: number // 距离缓冲点的时间间隔 停止追播
  pursueSpeed: number // 追播速度
  mode: 'pursue' | 'seek'
}

// 追播插件
export type PursueOptions = {
  enable: boolean
  flv?: PursueConfig
  hls?: PursueConfig
  native?: PursueConfig
}

export type ReportOptions = {
  enable: boolean
}

export type SwitchOptions = {
  enable: boolean
}

export type ScheduleOptions = {
  enable: boolean
  playerData: PlayerData
  debugUrl?: string // 调试指定资源
  debugCDN?: CDNNames // 指定CDN tx | ali | hw | cy
  debugPlayer?: PlayerTypes
}

export type Peer5Options = {
  enable: boolean
  customerId?: string
  fallback?: boolean
}

export type TextTrackInfo = {
  kind: string
  srclang: string
  src: string
  default?: boolean
  label?: string
}

// 字幕插件
export type VttOptions = {
  enable: boolean
  tracks?: TextTrackInfo[]
}

type LineMap = Record<CDNNames, string>
type QualityMap = Record<Quality, string>

// 皮肤插件
export type UIOptions = {
  line?: LineMap
  quality?: QualityMap
}

// 内核参数
export interface PureOptions {
  videoNode: string
  type: 'live' | 'vod'
  autoplay?: boolean
  controls?: 'custom' | 'native' | 'none'
  muted?: boolean
  poster?: string
  debug?: boolean | ILogger
}

// VhPlayer 参数
export interface Options extends PureOptions {
  appId: string
  accountId: string | number
  token: string
  language?: string
  liveOption?: LiveOption
  vodOption?: VodOption
  // 插件配置
  scheduleOption: ScheduleOptions
  pursueOption?: PursueOptions
  switchOption?: SwitchOptions
  marqueeOption?: MarqueeOptions
  watermarkOption?: WatermarkOptions
  barrageOption?: BarrageOptions
  reportOption?: ReportOptions
  peer5Option?: Peer5Options
  vttOptions?: VttOptions
  uiOptions?: UIOptions
}
```
