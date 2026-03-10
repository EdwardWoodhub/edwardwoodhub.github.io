---
title: 速度单位换算
---

# 速度单位换算Table

---

```sql speeds
-- 强制转换为数字并排除 0，确保对数轴激活
with long_data as (
    select cast(m_s as float) as m_s, km_h as val, 'km/h' as unit, scenario from speed_things.speed_conversion
    union all
    select cast(m_s as float) as m_s, mph as val, 'mph' as unit, scenario from speed_things.speed_conversion
    union all
    select cast(m_s as float) as m_s, knots as val, 'knots' as unit, scenario from speed_things.speed_conversion
)
select * from long_data 
where m_s > 0 
order by m_s
```

<ScatterPlot
    data={speeds}
    x="m_s"
    y="val"
    series="unit"
    xLog={true}
    yLog={true}
    xMin=1           xType=quantitative
    connected={true} markers={true}
    tooltipTitle="scenario"
/>

