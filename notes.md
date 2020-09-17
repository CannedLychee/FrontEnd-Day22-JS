**code1**

	判断是否为数字:
```javaScript
let num_check = function() {
	return !isNaN(num) && num 
}
```

	Math.abs() 绝对值
	Math.ceil() 向上取整
	Math.floor() 向下取整
	Math.max/min() 最大/最小值

**code4**

	深拷贝
```javaScript
function DeepCopy(obj) {
	if (!obj && typeof obj !== 'object') {
		throw new Error('输入不是对象')
	}
	const tragetObj = Array.isArray(obj)? []:{}
	for (let key in obj) {
		if (obj.hasOwnProperty(key)) {
			if (obj[key] && typeof obj[key] === 'object') {
				tragetObj[key] = DeepCopy(obj[key])
			}
			else {
				tragetObj[key] = obj[key]
			}
		}
	}
	return tragetObj
}
```

**code5**

	数组后端加元素 array.push(aa)	入队/入栈
	数组后端减元素 array.pop()		出栈
	数组前端加元素 array.shift(aa)	
	数组前端减元素 array.unshift()	出队
	