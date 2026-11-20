# 清明上河图 · 一卷长画的解说漫游

张择端《清明上河图》（北京故宫博物院藏）的深度缩放导览（中文解说）：绢本淡设色，24.8 × 528.7 厘米，从右往左读——郊野、漕船、虹桥、街市、城门与城内，卷尾是历代印章。整幅扫描（121,531 × 5,457 像素，含装裱与印章）是一张画布，附 20 个视图的导览。

Live: https://youdata.github.io/qingming-shanghe-zh/
English version: https://youdata.github.io/qingming-shanghe/. This page has no tiles of its own: it reads the pyramid from `../qingming-shanghe/qingming/` (the same origin on github.io).

Its fonts are in `fonts/`, trimmed to the page's characters. The narrated video is not included.

## How it is made

From `infographic-examples/qingming-documentary/build.mjs --lang zh`, with rx (`~/rx-cli`):

```sh
node build.mjs --lang zh                                           # → qingming-documentary-zh.json
rx export qingming-documentary-zh.json --out site --app /rx-graphic-editor/web/index.html --canvas --lock-layers --tiles dir --tile-base qingming=../qingming-shanghe/
rx publish site --to github:youdata/qingming-shanghe-zh --yes
```
