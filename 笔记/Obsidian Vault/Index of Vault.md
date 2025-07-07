# 📈 Progress log
```dataviewjs
let currentFolder = dv.current().file.folder;

dv.table(
  ["📄 文件", "🕒 创建时间", "🛠️ 修改时间", "📁 子路径"],
  dv.pages()
    .where(p => p.file.folder.startsWith(currentFolder) && p.file.name !== "README")
    .sort(p => p.file.mtime, 'desc')
    .map(p => [
      p.file.link,
      p.file.ctime.toFormat("yyyy-MM-dd HH:mm"),
      p.file.mtime.toFormat("yyyy-MM-dd HH:mm"),
      p.file.folder.replace(currentFolder + "/", "")
    ])
)
```
