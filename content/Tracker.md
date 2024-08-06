```dataviewjs
var a = moment().startOf('year');
var b = moment().endOf('year');

var n = moment()
var t = moment().startOf('day');

let q =  b.diff(a, 'days');
let p =  b.diff(t, 'days');
let r =  t.diff(a, 'days');

let h = n.diff(a, 'hours');
let i = b.diff(a, 'hours');

let html = `**THIS YEAR**         <progress style="height:10px;width:20%" value="`+h+`" max="`+i+`"></progress>`

if (r>0 && r<q) {
	html +=  `    ** ` +(h/i*100).toFixed(0)+`%** | `
	html +=  +p+` days remaining, `+ (p/7).toFixed(1)+ ` weeks remaining`
} else if (r==0) {
	html += `    **YEAR : ` +(h/i*100).toFixed(0)+`%** | `+ p + ` days remaining`
} else if (r==q) {
	html += `   Ends today`
} else if (r>q) {
	html += `   Ended `+-p+` days ago`
}else {
	html +=  `   `+-r+` days remaining`
}
dv.paragraph(html)
```

```dataviewjs
var a = moment().startOf('month');
var b = moment().endOf('month');


var n = moment()
var t = moment().startOf('day');

let q =  b.diff(a, 'days');
let p =  b.diff(t, 'days');
let r =  t.diff(a, 'days');

let h = n.diff(a, 'hours');
let i = b.diff(a, 'hours');

let html = `**THIS MONTH**     <progress style="height:10px;width:20%" value="`+h+`" max="`+i+`"></progress>`

if (r>0 && r<q) {
	html +=  `    **` +(h/i*100).toFixed(0)+`%** | `
	html += +p+` days remaining` 
} else if (r==0) {
	html += `    **` +(h/i*100).toFixed(0)+`%** | `+ p + ` days remaining`
} else if (r==q) {
	html += `   Ends today`
} else if (r>q) {
	html += `   Ended `+-p+` days ago`
}else {
	html += `   `+-r+` days remaining`
}

dv.paragraph(html)
```

```dataviewjs
var a = moment().startOf('week');
var b = moment().endOf('week');

var n = moment()
var t = moment().startOf('day');

let q =  b.diff(a, 'days');
let p =  b.diff(t, 'days');
let r =  t.diff(a, 'days');

let h = n.diff(a, 'hours');
let i = b.diff(a, 'hours');

let html = `**THIS WEEK**        <progress style="height:10px;width:20%" value="`+h+`" max="`+i+`"></progress>`

if (r>0 && r<q) {
	html +=  `    **` +(h/i*100).toFixed(2)+`%** | `
	html += +p+` days remaining  ` 
} else if (r==0) {
	html += `    **` +(h/i*100).toFixed(0)+`%** | `+ p + ` days remaining`
} else if (r==q) {
	html += `   Ends today `
} else if (r>q) {
	html += `   Ended `+-p+` days ago`
}else {
	html += `   `+-r+` days remaining`
}

dv.paragraph(html)
```

```dataviewjs
var a = moment().startOf('day');
var b = moment().endOf('day');

var n = moment()
var t = moment().startOf('day');

let q =  b.diff(a, 'days');
let p =  b.diff(t, 'days');
let r =  t.diff(a, 'days');

let h = n.diff(a, 'hours');
let i = b.diff(a, 'hours');
let j =  b.diff(t, 'hours');

let html = `**THIS DAY**           <progress style="height:10px;width:20%" value="`+h+`" max="`+i+`"></progress>`

if (r>0 && r<q) {
	html +=  `    **` +(h/i*100).toFixed(0)+`%** | `
	html += +p+` days remaining  ` 
} else if (r==0) {
	html += `    **` +(h/i*100).toFixed(0)+`%**`
} else if (r==q) {
	html += `   Ends today `
} else if (r>q) {
	html += `   Ended `+-j+` hours ago`
}else {
	html += `   `+-r+` days remaining`
}

dv.paragraph(html)
```
