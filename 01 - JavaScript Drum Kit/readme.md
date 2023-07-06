> 优化了一下这个 demo 的写法，原先是监听 `css动画` 的 `执行完成` 才去删除样式，是`固定`时间轴的。但是音频不可能都是固定长度，我的做法是监听视频的结束时间触发样式的删除

```javascript
audio.addEventListener(
  "ended",
  (e) => {
    key.classList.remove("playing");
  },
  { once: true }
);
```

其中 `{ once: true }` 是只监听一次的意思，不然会出现重复监听。

此外也复习了很多基础的东西

样式这一块的 `xxx.classList.add()`，`xxx.classList.remove()`，`xxx.classList.toggle()` 真的我都快忘了，原生我一般用的 style 去更改。
