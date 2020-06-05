# interview
记录一下自己碰到的面试题以及一些有趣的面试题


# 头条一面  2020/05/15

  1 js基础
  
  2 css 居中
  
  3 http 7层结构，option,跨域
  
  4 vue 父子生命周期，单向数据流
  
  5 顺时针打印矩阵

    const print = (arr) => {
        const tmparr = JSON.parse(JSON.stringify(arr))
        let result = [];
        console.log(tmparr);
        while (tmparr.length) {
            let temp = tmparr.shift();
            result = result.concat(temp);
            if (!tmparr.length) {
                return result;
            }
            for (let i = 0; i < tmparr.length - 1; i ++) {
                result.push(tmparr[i].pop());
            }
            temp = tmparr.pop().reverse();
            result = result.concat(temp);
            for (let i = tmparr.length - 1; i > -1; i --) {
                result.push(tmparr[i].shift());
            }
        }
        return result;
    }
