# YouCompleteMe Win64已编译版本
YouCompleteMe Windows 64已编译版本,支持C/C++补全,更为详细的问题请移步[https://github.com/ycm-core/YouCompleteMe](https://github.com/ycm-core/YouCompleteMe)

## 使用方法
使用vim-plug管理vim插件
```
if(has("win64"))
    Plug 'CaseZheng/Youcomplete'
endif
```

## 编译环境
1. python 3.7.4 64位
2. golang 1.14.1 64位
3. Visual Studio 2019
4. cmake 3.17.0
5. Windows10

## 依赖环境
1. vim 64位 需要支持python3[https://github.com/vim/vim-win32-installer](https://github.com/vim/vim-win32-installer)
2. python 3.7.4 64位
3. Visual Studio 2019（不安装无法补全标准库）

## 编译时命令
```
git clone --depth=1 https://github.com/ycm-core/YouCompleteMe.git
cd YouCompleteMe
git submodule update --init --recursive
python install.py --clang-completer --go-completer --msvc=16
```

## 编译时碰到问题
### 无法自动下载libclang
手动下载libclang放在指定目录即可
