# MornProcess

## 概要

OSプロセス実行ラッパー。ビルドやツール実行を非同期で管理するライブラリ。

## 依存関係

| 種別 | 名前 |
|------|------|
| 外部パッケージ | UniTask |
| Mornライブラリ | MornLib |

## 使い方

### Assetsディレクトリから実行

```csharp
var process = MornProcess.CreateAtAssets("git");
var output = await process.ExecuteAsync("status", ct);
```

### 相対パスから実行

```csharp
var process = MornProcess.CreateAtAssetsRelative("Tools", "mybuild.exe");
var result = await process.ExecuteAsync("--build", ct);
```
