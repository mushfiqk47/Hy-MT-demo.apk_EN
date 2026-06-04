# Hy-MT Demo - English Translation Patch

## Changes Made

### 1. UI Strings Chinese → English
All Chinese UI text translated to English in `res/values/strings.xml`:

| Original (Chinese) | Translated (English) |
|---|---|
| 腾讯混元翻译demo | Hunyuan Translate Demo |
| 取消 | Cancel |
| 确定 | OK |
| 下载 | Download |
| 清空输入 | Clear input |
| 关闭 | Close |
| 复制 | Copy |
| 已复制 | Copied |
| 翻译完成 | Translation complete |
| 翻译失败 | Translation failed |
| 翻译中… | Translating… |
| 离线翻译 | Offline Translation |
| 正在加载模型… | Loading model… |
| 结果由 AI 生成，仅供参考 | AI-generated results for reference only |
| 同意 | Agree |
| 拒绝并退出 | Decline & Exit |
| 使用协议 | License Agreement |
| 用户协议 | User Agreement |
| 开源协议 | Open Source License |
| 不再提醒 | Don't remind again |
| 请先下载模型 | Please download the model first |
| 暂不支持翻译此内容 | This content cannot be translated |
| 下载失败：%s | Download failed: %s |
| 正在下载 %1$s | Downloading %1$s |
| 该模型暂无下载地址，请联系开发者 | No download URL for this model. Contact developer. |
| 模型「%1$s」（约 %2$d MB）尚未下载，是否立即下载？ | Model "%1$s" (~%2$d MB) not downloaded. Download now? |
| 下载模型 | Download Model |
| （未下载） | (not downloaded) |

### 2. EULA / License Agreement Fully Translated
The entire end-user license agreement text (eula_message) was translated from Chinese to English, including all 6 clauses covering:
- AI-generated translation disclaimer
- On-device privacy guarantee
- Clipboard handling policy
- Liability waiver

### 3. Language Dropdown List Chinese → English
All 38 language names in the source/target language picker translated from Chinese to English in the app's compiled code (`smali/n2/d0.smali`):

| Chinese | English |
|---|---|
| 中文 | Chinese |
| 英文 | English |
| 法语 | French |
| 葡萄牙语 | Portuguese |
| 西班牙语 | Spanish |
| 日语 | Japanese |
| 土耳其语 | Turkish |
| 俄语 | Russian |
| 阿拉伯语 | Arabic |
| 韩语 | Korean |
| 泰语 | Thai |
| 意大利语 | Italian |
| 德语 | German |
| 越南语 | Vietnamese |
| 马来语 | Malay |
| 印尼语 | Indonesian |
| 菲律宾语 | Filipino |
| 印地语 | Hindi |
| 繁体中文 | Traditional Chinese |
| 粤语 | Cantonese |
| 波兰语 | Polish |
| 捷克语 | Czech |
| 荷兰语 | Dutch |
| 高棉语 | Khmer |
| 缅甸语 | Burmese |
| 波斯语 | Persian |
| 古吉拉特语 | Gujarati |
| 乌尔都语 | Urdu |
| 泰卢固语 | Telugu |
| 马拉地语 | Marathi |
| 希伯来语 | Hebrew |
| 孟加拉语 | Bengali |
| 泰米尔语 | Tamil |
| 乌克兰语 | Ukrainian |
| 藏语 | Tibetan |
| 哈萨克语 | Kazakh |
| 蒙古语 | Mongolian |
| 维吾尔语 | Uyghur |

## Technical Details

- **Method**: APK decompiled with `apktool 2.11.1`, resources and smali code patched, then rebuilt and signed
- **App package**: `com.tencent.hunyuan.angelslim`
- **Model**: Tencent HY-MT1.5 (on-device translation via llama.cpp/GGML)
- **Model weights**: [AngelSlim/Hy-MT1.5-1.8B-1.25bit](https://huggingface.co/AngelSlim/Hy-MT1.5-1.8B-1.25bit) on Hugging Face
- **Signed with**: Android debug key (requires uninstall of original app before install)
