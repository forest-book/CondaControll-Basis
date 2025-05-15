# CondaControll-Basis
anaconda(Windows) + python + githubで制御工学について勉強 <br>
特にanacondaを用いたpython仮想環境をgithubで管理・共有することを目的とする

## 仮想環境の起動コマンド
powershell,コマンドプロンプトで <br>
```
conda activate venv
```

## 仮想環境の終了コマンド
powershell,コマンドプロンプトで<br>
conda deactivate

## インストール済みモジュールの確認
conda list

## 環境をファイルに保存して記録
conda env export --from-history > environment.yml

## 共有されたファイルから環境を再構築
conda env create -f environment.yml
