```typescript
let arr: number[] = [1, 12, 1.23, 1.234, 1.2345]
let is10: boolean = false

arr.forEach(value => {
    console.log(value)
    if (value >= 10) {
        is10 = true
        return  // foeeach过程无法被终止
    }
})
console.log(is10)
/*输出结果
1
12    
1.23  
1.234 
1.2345
true  
*/
```

```typescript
arr.some(value => {
    console.log(value)
    if (value > 10) {
        is10 =  true
        return 1 //返回值为true跳出
    }
    return 0 //返回值为false继续
})
console.log(is10)
/*输出结果
1
12    
true  
*/
```

