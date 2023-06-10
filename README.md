# FSWorkbench
### Version 4.0 Preview

   
> **Note**   
正式版の場所でBeta版の公開を始めました。   
https://github.com/yamashita-software-works/FSWorkbench
   

FSWorkbenchは、コンピュータのハードディスクなどローカルストレージに含まれるファイルやディレクトリをGUIで表示・操作をするアプリケーションです。
ファイルシステムの情報を表示する他、コピー,移動,削除など基本的な操作も行えます。
ドライブの割り当てられていないボリュームを参照することも出来ます。

Version 4.0では、メインフレームウィンドウを旧来のMDIスタイルからタブ切り替えのTDIウィンドウに変更しました。
伝統的なWin32アプリケーションで、WinUIの様な最新のスキーム、デザインには対応していませんが、Windows 7、Windows 8.1やGUIが構成されたWindows RE/PEといった環境でも動作します。

**注:** 現状ではFSWorkbenchはオープンソースではありません。

**NOTICE:** FSWorkbench is not open source. You will find here the builds only. 

### 4.0.744.3 Preview

- ファイルリストで、"i"の様な幅の狭い一文字のディレクトリを選択するとタブに文字が表示されない不具合を修正。
- ファイルのタイムスタンプにミリ秒を表示した時、100ミリ秒以下の場合誤って表示される不具合を修正。

### 実行環境

Windows 10,Windows 8.1,Windows 7
(64bit版/32bit版)

### インストール

適切な場所にフォルダを作成し、書庫ファイルの内容を展開してください。<br>
他にファイルの存在しない、空のフォルダに展開することを強くお勧めします。

### 実行方法
展開した場所から、fsworkbench.exeを実行してください。

### アンインストール

現在アンインストーラは用意されておりませんので、展開したファイルをユーザーご自身で削除してください。

現在はアンインストールしてもレジストリキーがそのままになります。気になる場合はご自身でキーを削除してください。
FSWorkbench自身が使用するレジストリキーは以下の通りです。
 (他にWindowsが他のレジストリパスに記録することがあります)

      HKEY_CURRENT_USER\Software\YamashitaSoftwareWorks\FSWorkbench

### 使用条件

本ソフトウェアは、下記条件を承諾の上であれば自由に無償で使用できます。

- 本ソフトウェアはご利用になる方の責任で使用してください。
  作者及び頒布者は本ソフトウェアの実行によって生じる結果に関して一切の責任を
  負いません。

- 本ソフトウェアを操作した結果データが失われたり、ソフトウェアが表示した内容，
  実行環境の差異，未知の不具合などが原因で損害が生じた場合でも、作者及び頒布者
  は一切の責任を負いません。

- 本ソフトウェアは自由に再頒布できますが、再頒布時は書庫ファイル内のファイル,
  ディレクトリ構成はそのままで変更しないでください。

- ソフトウェアの性質上、コンピュータ上のファイルの削除や属性の変更、コピーに
  よる内容の上書きなど、ファイルに対して不可逆な操作も行えますので十分注意し
  て使用してください。

- 不具合等の連絡は、下記メールアドレスなどよりお願いします。

- 本ソフトウェアの著作権は作者が留保します。

  Copyright (C) 2015-2023 山下 克宏 (YAMASHITA Katsuhiro), Yamashita Software Works

***
This software is a preview/under development version.

FSWorkbench is a tool that displays information for files and directories on a local volume and performs simple operations. These operations are also available for volumes that do not have a drive assigned.
Not a "Filer" for comfortable user experience.

NOTICE:   
- THIS IS A PREVIEW VERSION. Technical specifications, features and the use thereof are subject to change or delete.
- Currentary, FSWorkbench is not open source. You will find here release builds only.
