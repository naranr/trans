# trans

#### Install
```
npm install -g 
```

#### Usage
1. 获取模版中文
```
trans get src/views/cart/index.vue
```
结果输出 i18n.cache/index.json，可以手动修改不正确的英文或者key

2. 设置模版key
```
trans set src/views/cart/index.vue
git diff src/views/cart/index.vue
```
设置后应该`git diff`查看语法是否正确。可以继续手动修改不正确的英文，但不能再修改key

3. 合并i18n.cache/*.json 到 src/lang/*.js
```
trans merge
git diff src/lang/*.js
```

4. 测试
```
npm run build:prod
```

#### Note
i18n.cache目录可以一直保留做全局key分析，但不需提交。
