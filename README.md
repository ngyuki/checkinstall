
## 概要

Fork from [http://checkinstall.izto.org/checkinstall.git](http://checkinstall.izto.org/checkinstall.git)

オリジナルの checkinstall に次の変更を行なっています。

 - installwatch.so のインストール先を x64 の場合は /usr/local/lib64 に変更
 - checkinstallrc のパスを /usr/local/etc に変更
 - デフォルトのインストールタイプに RPM を指定
 - デフォルトの除外ディレクトリに /selinux を指定

# インストール

```
git clone https://github.com/ngyuki/checkinstall.git
cd checkinstall/
make
make install
mkdir -p ~/rpmbuild/SOURCES
checkinstall --pkgversion=1.6.3
rpm -ivh ~/rpmbuild/RPMS/x86_64/checkinstall-1.6.3-1.x86_64.rpm
```
