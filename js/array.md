### reduce
[15.5, 2.3, 1.1, 4.7].reduce(function(total, num) {
	console.log(total, num);
    // 1 15.5
    // 17 2.3
    // 19 1.1
    // 20 4.7
    return total + Math.round(num);
}, 1); // 25