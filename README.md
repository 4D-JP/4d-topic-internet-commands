# 4d-topic-internet-commands
4D Internet Commands過去バージョンの公証についての考察

`otool -l`

||4D version|i386|x64|arm|
|:-:|:-:|:-:|:-:|:-:|
|sdk|v15|10.6|10.6|-|
|sdk|v17|10.6|10.12|-|

**ポイント**: 32-bit版のInternet Commandsは使用しているSDKが公証の最低ラインである`10.9`に満たないため，どのバージョンでも公証はできません。また，v17までは32-bit/64-bitのハイブリット版（Universal Binary）となっているため，そのままでは公証エラーとなります。64-bit専用のプラグインを用意する必要があります。

なお，v15は4DのSDKバージョンが`10.7`であるため，たとえアプリからプラグインを削除したとしても公証はできません。プラグインを改造することで公証できるのは，32-bitをサポートした最後のバージョン，v17だけです。

## 対策

[Releases](https://github.com/4D-JP/4d-topic-internet-commands/releases)に64-bit専用のプラグインを置きました。
