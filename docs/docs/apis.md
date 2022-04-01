```typescript
interface PlayerAPI {
  play(): Promise<void>

  pause(): void

  get isPaused(): boolean

  get isEnded() : boolean

  get isSeeking() : boolean

  set autoplay(v: boolean)

  get autoplay() : boolean

  get buffered() : TimeRanges

  get bufferedMax() : number

  get crossOrigin() : string | null

  set crossOrigin(v: string | null)

  get currentTime() : number

  set currentTime(t: number)

  set defaultMuted(v: boolean)

  get defaultMuted() : boolean

  get duration() : number

  set loop(v: boolean)

  get loop() : boolean

  get muted() : boolean

  set muted(b: boolean)

  get networkState() : number

  set playbackRate(v: number)

  get playbackRate() : number

  get played() : TimeRanges

  get preload() : string

  set preload(v: string) // 'auto' | 'metadata' | 'none'

  get readyState() : number // 0:没有任何信息，1：拥有元数据，2：当前位置播放数据可用，但是下一帧数据不够用，3：当前及下一帧数据可用，4，数据足够多，可以播放了

  get volume() : number

  set volume(v: number)

  get controls() : boolean

  set controls(v: boolean)

  get seekable() : TimeRanges

  // 宽带预估，单位：MB / s
  getEstimateNetSpeed() : number

  get cdnName() : string

  get quality() : Quality

  get qualities() : Quality[]

}
```
