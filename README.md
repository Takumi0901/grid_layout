## 対応ブラウザ
- Chrome 最新
- firefox 最新
- safari 最新
- IE9以上

[サンプルはこちら](https://s3-ap-northeast-1.amazonaws.com/102-design.sample/grid/index.html)

## 始めるには
``` html
<link rel="stylesheet" href="css/grid_layout.css">
```

## Grid Size
`grid__col--1`が最小単位
``` html
<div class="grid">
	<div class="grid__col grid__col--1">col</div>
	<div class="grid__col grid__col--1">col</div>
	<div class="grid__col grid__col--1">col</div>
	<div class="grid__col grid__col--1">col</div>
	<div class="grid__col grid__col--1">col</div>
	<div class="grid__col grid__col--1">col</div>
	<div class="grid__col grid__col--1">col</div>
	<div class="grid__col grid__col--1">col</div>
	<div class="grid__col grid__col--1">col</div>
	<div class="grid__col grid__col--1">col</div>
	<div class="grid__col grid__col--1">col</div>
	<div class="grid__col grid__col--1">col</div>
</div>
```

### 2カラム　レイアウト
``` html
<div class="grid">
	<div class="grid__col grid__col--6">col</div>
	<div class="grid__col grid__col--6">col</div>
</div>
```

### 3カラム　レイアウト
``` html
<div class="grid">
	<div class="grid__col grid__col--4">col</div>
	<div class="grid__col grid__col--4">col</div>
	<div class="grid__col grid__col--4">col</div>
</div>
```

### 4カラム　レイアウト
``` html
<div class="grid">
	<div class="grid__col grid__col--3">col</div>
	<div class="grid__col grid__col--3">col</div>
	<div class="grid__col grid__col--3">col</div>
	<div class="grid__col grid__col--3">col</div>
</div>
```

### 6カラム　レイアウト
``` html
<div class="grid">
	<div class="grid__col grid__col--2">col</div>
	<div class="grid__col grid__col--2">col</div>
	<div class="grid__col grid__col--2">col</div>
	<div class="grid__col grid__col--2">col</div>
	<div class="grid__col grid__col--2">col</div>
	<div class="grid__col grid__col--2">col</div>
</div>
```


##　Grid gutters
`grid--gutters`を付与
``` html
<div class="grid grid--gutters">
	・・・
</div>
```

## align
`grid__col`はdisplay:inline-block;なので文字と同じように右揃えや中央揃えができます。

### Grid right
``` html
<div class="grid grid--right">
	・・・
</div>
```

### Grid center
``` html
<div class="grid grid--center">
	・・・
</div>
```

## Grid justify
均等揃えも可能
``` html
<div class="container">
	<div class="grid grid--gutters grid--justify">
		<div class="grid__col grid__col--2"><div class="box">col</div></div>
		<div class="grid__col grid__col--6"><div class="box">col</div></div>
		<div class="grid__col grid__col--2"><div class="box">col</div></div>
	</div>
</div>
```

## Grid offset
要素のあとに指定col分の隙間
``` html
<div class="container">
	<div class="grid grid--gutters">
		<div class="grid__col grid__col--2 grid__offset--2"><div class="box">col</div></div>
		<div class="grid__col grid__col--6"><div class="box">col</div></div>
		<div class="grid__col grid__col--2"><div class="box">col</div></div>
	</div>
</div>
```

## Grid vertical-align



## Grid top
``` html
<div class="container">
	<div class="grid grid--gutters grid--top">
		<div class="grid__col grid__col--4">
			<div class="box">col<br>content<br>content</div>
		</div>
		<div class="grid__col grid__col--4">
			<div class="box">col</div>
		</div>
		<div class="grid__col grid__col--4">
			<div class="box">col</div>
		</div>
	</div>
</div>
```

## Grid middle
``` html
<div class="container">
	<div class="grid grid--gutters grid--middle">
		<div class="grid__col grid__col--4">
			<div class="box">col<br>content<br>content</div>
		</div>
		<div class="grid__col grid__col--4">
			<div class="box">col</div>
		</div>
		<div class="grid__col grid__col--4">
			<div class="box">col</div>
		</div>
	</div>
</div>
```


## Grid bttom
``` html
<div class="container">
	<div class="grid grid--gutters grid--bttom">
		<div class="grid__col grid__col--4">
			<div class="box">col<br>content<br>content</div>
		</div>
		<div class="grid__col grid__col--4">
			<div class="box">col</div>
		</div>
		<div class="grid__col grid__col--4">
			<div class="box">col</div>
		</div>
	</div>
</div>
```


## Grid nestd
``` html
<div class="container">
	<div class="container grid">
		<div class="grid__col grid__col--2 grid__offset--2">
			<div class="box">col</div>
		</div>
		<div class="grid__col grid__col--8">
			<div class="box">
				<div class="grid grid--right">
					<div class="grid__col"><div class="box">col1</div></div>
					<div class="grid__col"><div class="box">col2</div></div>
					<div class="grid__col"><div class="box">col3</div></div>
				</div>
			</div>
		</div>
	</div>
</div>
```

## カスマイズ
scss/_configs.scss内の変数を変更することでカスタマイズが可能。
``` scss
$var-breakpoint:				768px;
$var-col:						12;
$var-max-width:					100%;
$var-col-gutters:				2%;
```

[サンプルはこちら](https://s3-ap-northeast-1.amazonaws.com/102-design.sample/grid/index.html)