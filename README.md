# CondaControll-Basis
anaconda(Windows) + python + githubで制御工学について勉強 <br>
特にanacondaを用いたpython仮想環境をgithubで管理・共有することを目的とする

# Anaconda導入の背景
主にpython仮想環境での開発はpip(PyPL)を用いていたが、今回使用するpython制御工学ライブラリの<br>
**python-controll**に係り必要な**slycot**の導入がWindows環境では困難であった為、<br>
Anacondaによる開発を行うこととする
<br>
<br>
今回主に必要なライブラリ群
>Numpy<br>
>Scipy<br>
>Matplotlib<br>
>Sympy<br>
>Python-controll<br>
>slycot<br>

## 仮想環境の作成
Anaconda Promptにて<br>
```
conda create -n 環境名 python=バージョン
```

具体例<br>
```
conda create -n venv python=3.12
```

PowerShellやコマンドプロンプトでPythonを実行する場合<br>
Anaconda Promptにて
```
conda init
```
を実行

**conda init**実行後、PowerShellにて

>. : このシステムではスクリプトの実行が無効になっているため、ファイル `C:\~~~\WindowsPowerShell\profile.ps1` 
>を読み込むことができません。詳細については、
>「about_Execution_Policies」(https://go.microsoft.com/fwlink/?LinkID=135170)
>を参照してください。<br>
>発生場所 行:1 文字:3<br>
>`+` . `'C:\~~~\WindowsPowerShell\profile.ps1'`<br>
>`+`   `~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~`<br>
>    &emsp;`+` CategoryInfo          : セキュリティ エラー: (: ) []、PSSecurityException<br>
>    &emsp;`+` FullyQualifiedErrorId : UnauthorizedAccess

<br>が出る場合がある

## 仮想環境の起動コマンド
powershell,コマンドプロンプトで <br>
```
conda activate venv
```

## 仮想環境の終了コマンド
powershell,コマンドプロンプトで<br>
```
conda deactivate
```

## インストール済みモジュールの確認
```
conda list
```

## 環境をファイルに保存して記録
```
conda env export --from-history > environment.yml
```

## 共有されたファイルから環境を再構築
```
conda env create -f environment.yml
```
