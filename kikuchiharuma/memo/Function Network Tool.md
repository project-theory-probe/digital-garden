## プロトタイプのアイディア

- 無限の中にいきなり function / point を作る (call) することができる
	- function
		- point a を point b に変換する作用の名称
		- 合成できる
		- 引き算できる
		- 他の function と比較できる
	- point
		- 合成しても引き算しても結果に影響しない
		- 他の point と比較できる
		- (空の作用を持った function とどう違う？)
- 座標を定義しない
	- function を直接 call し、互いに関連づけるツール
	- 座標がないので点の相対的な距離は不明
	- ツールは function と point が一致するかしないか、だけを扱う
		- 名前の一致する function と point は一致しなければならない
			- ただし、コンテキスト (名前空間) がある
			- 別のコンテキストであれば同じ名前が存在できる
		- 一致しているかどうか =  同じ名前で良いかの判断は直感に委ねる
			- 一致していてはいけない -> 別の名前を探す
	- 名指しの効果に期待する＝名前が与えられる前の状態は無限

![[function-network-tool-00.png]]

- ツール上に function の存在を仮定する
	- 完全でなくても良い
		- 始点、終点、差分
			- 入力、出力、作用
			- initial point 、terminal point 、vector
		- どの部分からでも仮置き
	- 不完全な function を補うために考えるプロセスがワークフローの中心
		- function F
			- 現実世界における変化の表現
				- 始点と終点の関係
				- 相対的な表現
				- エネルギーや質量の大小は問わない
			- ひとつの変化 (function) を追加する度に
				- 3つの区別を生じる＝名指す機会が生じる
					- これがこのツールがユーザに要求する唯一のこと
					- 制約でもあり、ユーザを支援する手法でもある
				- 名指す機会はさらに別の function の存在を示唆する
					- 既存の point を終点・始点とするあらゆる function があり得る

![[function-network-tool-01.png]]

- path の発展イメージ
	- path = point を共有する複数の function 
	- AS-IS - TO-BE を結ぶ作用を仮置きする
		- function F
			- point A
	- 周辺に関係しそうな as-is - to-be を置く
		- point a / point b
		- function で関係づけられるまで互いの位置関係は不明
			- ツール上は、直感に従って自由に配置してよい
	- 各 point を function で結ぶ
		- 各 point の相対位置を知ることができる
			- point A 
				- function ( point a -> A ) と function ( point b -> A ) を両立する点
			- point b から TO-BE までの相対位置
				- point b から TO-BE に変換する function ＝ point A + function F - point b
		- 必ずしも時間軸や意図の進行方向と合成の方向は一致しない
			- 現在 (らしい) point を起点に過去の point へ変換する function があり得る
	- 上記は一例
		- AS-IS - TO-BE から始まらなくてもよい
		- F の作用から始め、何に適用するかを検討することもできる

![[function-network-tool-02.png]]

- path の詳細化イメージ
	- function を複数の function の合成で置き換える
		- マイルストーンに分割するイメージ
	- 分割されると、point が増える
		- 潜在的な point to point = function が増える
	- 例えば
		- 新しいマイルストーンを作成し、各ロールの役割を検討する場面
			- function と point で表現すると
				- A1 を始点、 A2 を終点とする F
				- A1 を始点とするより小さい f1 で到達可能な A1-2 を作る
				- a1-2 / b1-2 を始点として A1-2 を終点とする function を考える
			- 以降繰り返すことで A2 へ到達する path を積み上げていく
				- [[アジャイル]]の一般的なプロセス

![[function-network-tool-03.png]]

- 自律チームの構造
	- 期待されるチームの働きを仮置き
		- function F (point A -> point A')
	- a, b, c, d, e は個人または間接的な成果物の状態を名指す point
		- function ( a -> A ) が、a による A のチーム状態に対する貢献を定義する
			- 人や成果物が、チームの状態に含まれているわけではない
			- 独立に存在した上で関係づけられる
		- point A について、これらの point との相対位置を知ることができる
	- a, b, c, d, e と A を結ぶ各 function が変わらない場合
		- a, b, c, d, e すべてに function F 相当の作用を加えると a', b', c', d', e' へ平行移動する
		- A’ の相対位置
			- a', b', c', d', e' それぞれに a, b, c, d, e と A を結ぶ各 function の合成
	- a', b', c', d', e' に到達するためにどんな path を持っていてもよい
		- path の形を関わりなく、自己完結的に F 相当の働きをすることができる (自律)
- 自律的でない場合
	- point A に対して複雑な path でつながった point の群
		- 多数の function を経由して point A にアクセスする
			- point A が動けば末端も動くことができる
				- 目的に対する倒錯が起こる
			- 自律チームの場合は周辺の軽い (function の依存関係が小さい) point が先に動く
				- 結果として A に作用し A' へ変換する

![[function-network-tool-04.png]]

- 多数のユーザの連携
	- それぞれのユーザが独自の無限の空間 = function newtwork をもつ
	- 無限の空間の中でできることは、好きな名前を call すること
		- call されたものは function か point として存在しはじめる
	- ユーザはほかのユーザに向かって call することもできる
		- 相手の空間の中に function か point を存在させることができる (対話)
			- 一般に、point
				- (別の network で同様に機能する function を作ることは非常に難しい)
		- 対話する際、そのユーザがすでに持っている function network と調和させる必要がある
			- function / point はユニークでなければいけない
	- functor
		- call によって共有された point を原点にして他者の function network を投影する
			- 他のユーザの function network の一部しか知ることができない
				- call によって共有された＝対話の対象になった＝矛盾が解消されている範囲
			- また自分のネットワークの影響を受けて歪む
				- 自分の知り得る point や function との相対位置に置くと
				- 相手のそれとは異なった配置になる
			- 現在のほとんどの現場ではこの投影の問題は経験や勘によって対処されてるはず
				- 直線的に進む F が小さい f に分割されるというタイムボックスのアイディアは
				- 投影をやりやすくする工夫と考えられる
					- 分割された点に対して自分の function network を構造化し
					- その点を起点にしてチームメイトの function network にアクセスする
				- 自動的に命名されるという点も負荷を下げそう
					- 来週、次回、といった名前
						- 内容に関わる必要がなく
						- 解釈のズレが起こりづらい
					- タイムボックスがないと
						- 互いの function network を知るためにまず互いの function network を知るという地獄のループに陥る