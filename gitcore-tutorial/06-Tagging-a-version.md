```aa

　　　　　　　　　　　／.:.:.　　　　　　　　 ＼
　 　 　 　 　 　 　 /:,:.:.:　 ／　　　ヽ　　　　＼
　　　　　　　　　 /.:.l:.:.:/:/　　　:/ 　',　:l　　 ヾ`ｰ
　 　 　 　 　 　 /!:.:.|:.: l/　 〃 /　j　}　:|　 　 ﾊ
　　　　　　　　/ｲ:.:.i|:.:.jL∠/_/ | /l.ﾑ_/|　l 　ｌ }　　…git のタグには
　　　　　　　　　N:.ﾊ:.:.:lｨfｱﾄ/　ﾚ　ｨ=ﾄ | /| ∧j　　 　　 「軽い(light)」タグと
　　　　　　　　　　ヽﾑ:.} ii;_j　　　　ii;ﾘ ﾙ iﾚヽ.　　　　「説明つき(annotated)」タグの2種類ある
　 　 　 　 　 　 　 　 `ﾍ:ゝ　　　_ 　 　 小/　　　　　
　 　 　 　 　 　 　 　 　 ヾ:{＞､ _　ｨ＜}/|/　　　　　　軽いタグというのは単にブランチと同じものと言っていい
　　　　　　　　　　 _, ｨr'´ヽ｛ __＿`}　ヽ､_　　　
　　　　　　　　　／| l:|　　　| =＝=|　　 |:lﾞヽ　　　
　　　　　 　 　 /　 | l:ｌ　　　l 　 　 l　　 l::ｌ　l
　　 　 　 　 　 l　　ヽﾊ　 　 l　 　 l　　//　 |
```
```
$ git tag my-first-tag
```
```aa
　　 　 ,　'´￣￣｀ ｰ-､　　　　　
　　 ／　　 〃" ｀ヽ､　＼　　　　
　 /　/　 ﾊ/　　　　 ＼ﾊﾍ　　　このコマンドは HEAD を .git/refs/tags/my-first-tag というファイルに書き込むだけだよ！
　 |i │ ｌ |ﾘノ　　　 ｀ヽ}_}ハ.　　　
　 |i　|　从 ● 　 　 ●ｌ小N　　　こうやっておくことであとからこの時点のコミットを参照できるのさっ
　 |i （|　⊂⊃ ､_,､_,　⊂lｉ|ノ　　 　
　 | i⌒ヽ j　　（_.ノ 　　ﾉi|__／⌒)　
　 | ヽ 　ヽx＞､ __,　イｌ　|::::ヽ／.　 
　 |　∧__,ﾍ}::ﾍ三|:::::/ｌ|　|',:::::ﾊ　　
　 |　ヾ_:::ッﾘ :::∨:／　|　| >'''´
```
```
$ git diff my-first-tag
```
```aa
　　　　　　　　　　　／.:.:.　　　　　　　　 ＼
　 　 　 　 　 　 　 /:,:.:.:　 ／　　　ヽ　　　　＼
　　　　　　　　　 /.:.l:.:.:/:/　　　:/ 　',　:l　　 ヾ`ｰ
　 　 　 　 　 　 /!:.:.|:.: l/　 〃 /　j　}　:|　 　 ﾊ
　　　　　　　　/ｲ:.:.i|:.:.jL∠/_/ | /l.ﾑ_/|　l 　ｌ }　　こうすると後から今の時点との diff を見ることができる
　　　　　　　　　N:.ﾊ:.:.:lｨfｱﾄ/　ﾚ　ｨ=ﾄ | /| ∧j　　 　　 
　　　　　　　　　　ヽﾑ:.} ii;_j　　　　ii;ﾘ ﾙ iﾚヽ.　　　もちろん今は何も出力されない
　 　 　 　 　 　 　 　 `ﾍ:ゝ　　　_ 　 　 小/　　　　　
　 　 　 　 　 　 　 　 　 ヾ:{＞､ _　ｨ＜}/|/　　　　　
　　　　　　　　　　 _, ｨr'´ヽ｛ __＿`}　ヽ､_　　　
　　　　　　　　　／| l:|　　　| =＝=|　　 |:lﾞヽ　　　
　　　　　 　 　 /　 | l:ｌ　　　l 　 　 l　　 l::ｌ　l
　　 　 　 　 　 l　　ヽﾊ　 　 l　 　 l　　//　 |

　 　　　＿＿＿_　　
　　　／　　 　 　＼
　 ／　　─　 　 ─＼　　　　なるほど…。.git/refs/heads/* はコミットの度に新しいSHA1が刻まれるが
／ 　　 （●） 　（●） ＼　　tags/* にその時点でのコミットを保存しておいて
|　 　　 　 （__人__）　 　 |　　後から参照できるようにするということかお
/　　　　 ∩ノ ⊃　　／
(　 ＼　／ ＿ノ　|　 |
.＼　“　　／＿＿|　 | 　
　　＼ ／＿＿＿ ／ 　 


　　　　　　　　　　　／.:.:.　　　　　　　　 ＼
　 　 　 　 　 　 　 /:,:.:.:　 ／　　　ヽ　　　　＼
　　　　　　　　　 /.:.l:.:.:/:/　　　:/ 　',　:l　　 ヾ`ｰ
　 　 　 　 　 　 /!:.:.|:.: l/　 〃 /　j　}　:|　 　 ﾊ
　　　　　　　　/ｲ:.:.i|:.:.jL∠/_/ | /l.ﾑ_/|　l 　ｌ }　　説明つきタグは git のオブジェクト
　　　　　　　　　N:.ﾊ:.:.:lｨfｱﾄ/　ﾚ　ｨ=ﾄ | /| ∧j　　 　　 
　　　　　　　　　　ヽﾑ:.} ii;_j　　　　ii;ﾘ ﾙ iﾚヽ.　　　tree にコミットメッセージを付けて commit オブジェクトが生成されたように
　 　 　 　 　 　 　 　 `ﾍ:ゝ　　　_ 　 　 小/　　　　　commit にメッセージや署名を加えて tag オブジェクトを生成する
　 　 　 　 　 　 　 　 　 ヾ:{＞､ _　ｨ＜}/|/　　　　　
　　　　　　　　　　 _, ｨr'´ヽ｛ __＿`}　ヽ､_　　　
　　　　　　　　　／| l:|　　　| =＝=|　　 |:lﾞヽ　　　
　　　　　 　 　 /　 | l:ｌ　　　l 　 　 l　　 l::ｌ　l
　　 　 　 　 　 l　　ヽﾊ　 　 l　 　 l　　//　 |
```
```
$ git tag -s <tagname>
```
```aa
　 　　　／⌒　　⌒＼
　　　／（ ●） 　（●）＼　　またエディタが起動したお！
　 ／::::::⌒（__人__）⌒::::: ＼　ここにリリース用のメッセージなんかを書けばいいお？
　 |　　　　　|r┬-|　　　　　|　ZZ で保存だお！
　 ＼ 　　 　 `ー'´ 　 　 ／

　 　 　　　＿＿＿_
　 　　　／ノ 　 ヽ､_＼
　　　／（ ○）}liil{（○）＼
　 ／　　　 （__人__）　　　＼　なんかエラーが出たお！
　 |　　　ヽ　|!!il|!|!l|　/　　　|
　 ＼　　　　|ｪｪｪｪ| 　 　 ／


　　 　 ,　'´￣￣｀ ｰ-､　　　　　
　　 ／　　 〃" ｀ヽ､　＼　　　　
　 /　/　 ﾊ/　　　　 ＼ﾊﾍ　　　-s は PGP 署名をするから ちゃんと設定してないとエラーが出るかもね
　 |i │ ｌ |ﾘノ　　　 ｀ヽ}_}ハ.　　-a でやれば署名をしないよっ
　 |i　|　从 ● 　 　 ●ｌ小N　　　
　 |i （|　⊂⊃ ､_,､_,　⊂lｉ|ノ　　 　
　 | i⌒ヽ j　　（_.ノ 　　ﾉi|__／⌒)　
　 | ヽ 　ヽx＞､ __,　イｌ　|::::ヽ／.　 
　 |　∧__,ﾍ}::ﾍ三|:::::/ｌ|　|',:::::ﾊ　　
　 |　ヾ_:::ッﾘ :::∨:／　|　| >'''´


　 　 　　　＿＿＿_
　 　　　／⌒　　⌒＼　　なんだお！
　　　／（ ●） 　（●）＼　　そういう事は先に言うお！
　 ／::::::⌒（__人__）⌒::::: ＼　
　 |　　　　　|r┬-|　　　　　|　
　 ＼ 　　 　 `ー'´ 　 　 ／

```
```
$ git tag -a my-annotated-tag
```
```aa
　　 　 ,　'´￣￣｀ ｰ-､　　　　　
　　 ／　　 〃" ｀ヽ､　＼　　　　
　 /　/　 ﾊ/　　　　 ＼ﾊﾍ　　　.git/refs/tags/my-annotated-tag は tag オブジェクトへの参照になっているはずだよっ
　 |i │ ｌ |ﾘノ　　　 ｀ヽ}_}ハ.　　
　 |i　|　从 ● 　 　 ●ｌ小N　　　
　 |i （|　⊂⊃ ､_,､_,　⊂lｉ|ノ　　 　
　 | i⌒ヽ j　　（_.ノ 　　ﾉi|__／⌒)　
　 | ヽ 　ヽx＞､ __,　イｌ　|::::ヽ／.　 
　 |　∧__,ﾍ}::ﾍ三|:::::/ｌ|　|',:::::ﾊ　　
　 |　ヾ_:::ッﾘ :::∨:／　|　| >'''´
```
```
$ git cat-file -t `cat .git/refs/tags/my-first-tag`
commit
$ git cat-file -t `cat .git/refs/tags/my-annotated-tag`
tag
```
```aa
　　　　　　　　　　　／.:.:.　　　　　　　　 ＼
　 　 　 　 　 　 　 /:,:.:.:　 ／　　　ヽ　　　　＼
　　　　　　　　　 /.:.l:.:.:/:/　　　:/ 　',　:l　　 ヾ`ｰ
　 　 　 　 　 　 /!:.:.|:.: l/　 〃 /　j　}　:|　 　 ﾊ
　　　　　　　　/ｲ:.:.i|:.:.jL∠/_/ | /l.ﾑ_/|　l 　ｌ }　　…説明つきタグはリリース時に
　　　　　　　　　N:.ﾊ:.:.:lｨfｱﾄ/　ﾚ　ｨ=ﾄ | /| ∧j　　 　　 軽いタグは自分用に使うといい
　　　　　　　　　　ヽﾑ:.} ii;_j　　　　ii;ﾘ ﾙ iﾚヽ.　　　
　 　 　 　 　 　 　 　 `ﾍ:ゝ　　　_ 　 　 小/　　　　　
　 　 　 　 　 　 　 　 　 ヾ:{＞､ _　ｨ＜}/|/　　　　　
　　　　　　　　　　 _, ｨr'´ヽ｛ __＿`}　ヽ､_　　　
　　　　　　　　　／| l:|　　　| =＝=|　　 |:lﾞヽ　　　
　　　　　 　 　 /　 | l:ｌ　　　l 　 　 l　　 l::ｌ　l
　　 　 　 　 　 l　　ヽﾊ　 　 l　 　 l　　//　 |


　　 　 ,　'´￣￣｀ ｰ-､　　　　　
　　 ／　　 〃" ｀ヽ､　＼　　　　
　 /　/　 ﾊ/　　　　 ＼ﾊﾍ　　　これで git の 4種類のオブジェクトが全部出てきたね！
　 |i │ ｌ |ﾘノ　　　 ｀ヽ}_}ハ.　　次はリポジトリの移動についてだよっ！
　 |i　|　从 ● 　 　 ●ｌ小N　　　
　 |i （|　⊂⊃ ､_,､_,　⊂lｉ|ノ　　 　
　 | i⌒ヽ j　　（_.ノ 　　ﾉi|__／⌒)　
　 | ヽ 　ヽx＞､ __,　イｌ　|::::ヽ／.　 
　 |　∧__,ﾍ}::ﾍ三|:::::/ｌ|　|',:::::ﾊ　　
　 |　ヾ_:::ッﾘ :::∨:／　|　| >'''´
```

