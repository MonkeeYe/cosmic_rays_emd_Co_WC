# cosmic_rays_emd_Co_WC
---
# Geomagnetic Storm Forecasting caused by ICME based on CEEMDAN of Cosmic rays article layout
[toc]
## Overview
- Method: CEEMDAN/Hilbert Transform
- Cosmic Rays/Kp IndexDataset
  - Time Range: Solar Cycle 22/1997-2008, Solar Cycle 23/2008-2019
  - Time Resolution: 0.5h/3h
- Event Requirement:
  - Kp > 8
---
## Data Preprocessing
1. ICMEs -> 4 days before events
2. CRs -> CEEMDAN -> 1-10 IMFs

```flow
st=>start: 开始
e=>end: 结束
op1=>operation: 新品开发流程
op2=>operation: 产品需求提出
op3=>operation: 产品试用 负责人：吴xx
op4=>operation: 包装
op5=>parallel: 继续讨论
op6=>operation: 讨论
cond=>condition: 确认？

st->op1->op2->op3->cond
cond(yes)->op4->e
cond(no)->op6->e
```

1. IMF(s) Ma->
2. data quality -> error situation statistic
3. check the data distribution -> show in figure or table
4. color removing and masking
5. fits/jpeg -> [0,1]
---
## Methodology
NO-SUM
1. statics
    |Num.|Max|Min|Mean|
    |--|--|--|--|
    |IMF|?|?|?| 
2. time-domain:
- x: time(3h), y:imf, z:max/min/mean -> (threshold)
3. frequency-doamin:
   - x: frquency(Hz), y: imf, z: amplitude
   - x: time(3h), y: imf, z: max amplitude/index of max amplitude
## Validation \& Result
- in advance? how long?
- *quiet period -> warning signal?
- test on new data： Solar Cycle 22/1997-2008, Solar Cycle 23/2008-2019
---
> Figures  
>   1. CRs 11 year-period compare with SSN
>   2. Diurnal variation
>   3. CEEMDAN robust(compared with emd \& eemd)
>   4. methdology 2/3
>   5. test result
> 