# VVVF-Inverter
Transphorm製のGaNFETを使ったドレミファインバーターの簡易版です。
注意
本リポジトリは、GaN三相インバータ設計の学習・研究のための記録です。夏休みに一ヶ月半で作りました。絶対にマネしないでください。
![本体](https://github.com/Yoshio-Kamada/VVVF-Inverter-GaN/blob/main/IMG_2794.JPG)
裏側にはスナバ回路を設けました。
※配線ミスの補修をしています。
![裏側](https://github.com/Yoshio-Kamada/VVVF-Inverter-GaN/blob/main/IMG_2795%20(1).JPG)
マイコン側とゲートドライバと主回路はフォトカプラと絶縁コンバーター＋ブートストラップで絶縁しました。
主回路部分はパターンを太くしました。
![pcb](https://github.com/Yoshio-Kamada/VVVF-Inverter-GaN/blob/main/PCB_PCB_3phase-inverter_2026-01-07.jpg)
設計に甘い箇所・見落とし・ミスが複数あり、安全性が十分検証できていないため、ガーバーファイル等製造データは意図的に公開していません。あくまで設計思想・苦労した点の技術記録としてご覧ください。
## プログラムコードの参照元について

本プロジェクトの制御プログラムは、三相インバータ制御の参考として公開されている  
[naoto64/Three-phase-inverter](https://github.com/naoto64/Three-phase-inverter) をベースにしています。  
同リポジトリには AC100V 三相インバータの動作コードが MIT ライセンスで公開されており、`VVVF‑Inverter‑GaN` 側ではこれを GaN デバイス向けに改変・最適化しています。

元コードの詳細やライセンス条項については、参照元リポジトリの README および LICENSE をご確認ください。






