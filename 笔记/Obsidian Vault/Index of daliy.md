```dataview
table 今日简要记录, 情绪变化, 明天目标, file.day as 日期
from "3_Diary"
where 今日简要记录 and 情绪变化 and 明天目标
sort file.day desc
```

