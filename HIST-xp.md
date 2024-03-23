
准备仓库

```ps1
git clone --single-branch --branch py/dramatiq https://gitee.com/flowark/oss-fork.git dramatiq
cd dramatiq
git remote add upstream https://github.com/Bogdanp/dramatiq.git
```

准备 venv

```ps1
python -m venv .venv
. .venv/Scripts/activate
python -m pip install -U pip wheel setuptools build
```

升级上游

```ps1
git fetch upstream v1.17.1
git rebase FETCH_HEAD

# 修改 dramatiq\__init__.py :: __version__
```

开始构建

```ps1
python -m build
```
