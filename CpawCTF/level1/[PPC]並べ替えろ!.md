### Description
下にある配列の中身を大きい順に並べ替えて、くっつけてcpaw{並べ替えた後の値}をフラグとして提出してください。
例：もし配列｛1,5,3,2｝っていう配列があったら、大きい順に並べ替えると｛5,3,2,1}となります。
そして、フラグはcpaw{5321}となります。
同じようにやってみましょう（ただし量が多いので、ソートするプログラムを書いたほうがいいですよ！）
### Writeup
ソートするだけ。以下はpythonのサンプルコード。ただし長いので入力は省略している。
```
x = [...]
print("".join(map(str,reversed(sorted(x)))))
```
