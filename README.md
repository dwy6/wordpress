# WordPress 镜像仓库（github.com）

> 由 WP-Mirror-Sync 自动同步生成
> [dwy6/wordpress](https://github.com/dwy6/wordpress)

- 当前最新版本: **7.0.4**
- 同步时间: **2026-08-20 00:38:29**
- 分支: **main**

## 目录结构

```
data/
+-- latest/             # 最新版本快捷入口
|   +-- wordpress.zip          相对路径软链接（git clone 后用）
|   +-- wordpress-latest.zip   实际文件副本（raw 下载用）
|   +-- VERSION                  版本号文本
+-- archive/           # 历史版本存档
|   +-- 7.0.4/
|   |   +-- wordpress-7.0.4.zip
+-- meta/              # 文件元数据
    +-- 7.0.4/
        +-- meta.json
checksums.json         # 全量校验和记录
sync_state.json        # 同步状态
```

## 使用方式

### 获取最新版本

**Git clone 后使用（推荐）:**

```bash
git clone https://github.com/dwy6/wordpress.git
cp data/latest/wordpress.zip ./wordpress.zip
```

**Raw 直链下载:**

```bash
curl -L -o wordpress.zip "https://raw.githubusercontent.com/dwy6/wordpress/main/data/latest/wordpress-latest.zip"
```

**按版本下载:**

```bash
curl -L -o wordpress.zip "https://raw.githubusercontent.com/dwy6/wordpress/main/data/archive/7.0.4/wordpress-7.0.4.zip"
```

### 获取指定版本

从 tag 获取:

```bash
git clone https://github.com/dwy6/wordpress.git --branch v7.0.4
```

### 验证文件完整性

```bash
# 查看校验和
cat data/meta/7.0.4/meta.json

# 本地校验
sha256sum wordpress-7.0.4.zip
md5sum wordpress-7.0.4.zip
```

---

*同步系统: WP-Mirror-Sync*
*维护者: 呆窝云 <service@dwoyun.com> | https://dwoyun.com*