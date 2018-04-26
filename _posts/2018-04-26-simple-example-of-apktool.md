---
layout: post
title: Simple Examples of Apktool
featured-img: sleek
mathjax: true
---

## Apktool

[Apktool](https://ibotpeaches.github.io/Apktool/) can decode resources to nearly original form and rebuild them after making some modifications.

### Decode

```
apktool d test.apk

```

### Build

```

apktool b test

```

### Force Example

If error in build like '@android:style/Animation.OptionsPanel', run this before build. Ref [Issue #1745](https://github.com/iBotPeaches/Apktool/issues/1745).

```

apktool empty-framework-dir --force

```
