# FSWorkbench-Preview

このソフトウェアは[FSWorkbench](https://github.com/yamashita-software-works/FSWorkbench/releases)のプレビュー版または開発中のものです。
安定版は[こちら](https://github.com/yamashita-software-works/FSWorkbench/releases)から入手してください。

### 注意
- これはプレビューバージョンです。**プレビューバージョンで実装されている仕様や機能は変更・削除される可能性があります。** また、ビルドを頻繁に更新する場合があります。

- 現在のところFSWorkbenchのソースコードは公開していません。


### 動作環境

Windows 7 (x64,x86)   
Windows 10 (x64,x86)   
Windows 11 (x64)    


### Version 3.4の変更点

- ナビゲーションペインの変更   
  従来タブで切り替えていたナビゲーションペインのページを、ウィンドウ左端に設けた「Outlookバー」状のボタンで切り替える様にしました。ページはメインメニューからも切り替えできます。
  それに伴い、ナビゲーションペインに以下のページを追加（一部はデフォルトで非表示）しました。   
  ※これらは仮称です。また正式版では削除・変更させる可能性があります。

  - ファイルリスト   
    表示中のファイルリストウィンドウの一覧が表示ます。ウィンドウ タブと同じ機能です。

  - 場所   
    ボリューム、ドライブ、シェルフォルダの一部、ブックマークをグループ化して表示するページです。   
    userfolders.iniに定義されています。
  
  - お気に入り   
    お気に入りに登録された項目が表示されますが、現状編集する手段を提供していません。   
    手作業で以下の場所にファイルを作成するか、旧バージョンFSDirWalkerが作成したファイルをコピーしてください。
    ```
    %LOCALAPPDATA%\FSTools\FSWorkbench\favorites.xml
    ```   
    %LOCALAPPDATA%は通常、"C:\Users\\_UserName_\AppData\Local" の様なパスになります。   
    favorite.xmlの内容は以下の様になります。なお、現在の書式は旧バージョンのままのため、将来変更される可能性があります。

    ```
    <?xml version="1.0" encoding="UTF-8"?>
    <Favorites>
      <Directories>
        <Path>\??\C:\Windows\System32\Drivers</Path>
      </Directories>
      <Files>
        <Path>\??\C:\Foo\bar\mytext.txt</Path>
        <Path>\Device\HarddiskVolume2\Windows\System32\notepad.exe</Path>
      </Files>
    </Favorites>
    ```
    パスはデバイス形式（オブジェクトネームスペースの\Device\HarddiskVolume*N*の様な形式）で指定する必要があります。ボリュームデバイスに割り当てられる番号は一定でない場合があるので、オブジェクトネームスペースのDosDeviceプリフィックス"\??\"を付けたドライブ（"\??\C:\Foo\bar"の様な）で指定することをお勧めします。
  
  - ディレクトリツリー   
    通常は表示されません。表示するにはレジストリで設定を追加する必要があります。現状ディレクトリツリーは表示したいディレクトリを選択するナビゲーション機能のみ動作します。ファイルをドロップしたり、ディレクトリを削除するなどの操作はできません。またディレクトリの増減、リネームなどの変化にも追従しないので、必要な時に更新ボタンを押して表示を更新する必要があります。
  

- ファイルリストの[表示の種類]にタイル表示を追加   

  ファイルリストの[表示の種類]に[タイル]と[サムネイルタイル]を追加しました。   
  現在、デフォルトでタイルにファイル名のみ表示されます。タイル表示時に更新日付とサイズを表示したい場合は、レジストリに以下の値を追加します。   

    ```
    HKEY_CURRENT_USER\SOFTWARE\YamashitaSoftwareWorks\FSWorkbench\Workspace\{00000001-0000-0000-0000-000000000000}\.default\{81000001-0001-0000-0000-000000000000}\FileList

    EnableMultiLineTile(REG_DWORD)=0x1
    ```
<BR>

***
This software is a preview/under development version of [FSWorkbench](https://github.com/yamashita-software-works/FSWorkbench/releases).

FSWorkbench is a tool that displays information for files and directories on a local volume and performs simple operations. These operations are also available for volumes that do not have a drive assigned.
Not a "Filer" for comfortable user experience.

NOTICE:   
- THIS IS A PREVIEW VERSION. Technical specifications, features and the use thereof are subject to change or delete.
- Currentary, FSWorkbench is not open source. You will find here release builds only.
