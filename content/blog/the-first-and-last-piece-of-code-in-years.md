---
title: "每年的第一段和最后一段代码"
slug: "the-first-and-last-piece-of-code-in-years"
author: "Bin Hua"
date: 2024-01-01T04:33:21Z
tags: ["code", "代码", "程序员"]
draft: false
---

刚才锻炼的时候突然想到一个问题，是不是记录下以后每年写的第一行（段）和最后一行（段）代码？感觉是个有意思的事情，就从 2024 年开始吧。

#### 2025 年

第一段代码写于 2024 年 01 月 01 日，在东京的酒店写的，这段代码用于一款 AR 的 iOS 应用，用户部分的 Model。这款应用会在一个月内上线，采用快速迭代的方式

```
struct User: Codable, Identifiable {
    let id: String
    let email: String
    var username: String
    var profileImageUrl: String?
    
    enum CodingKeys: String, CodingKey {
        case id
        case email
        case username
        case profileImageUrl = "profile_image_url"
    }
}
```

#### 2024 年

第一段代码写于 2024 年 01 月 01 日，这段代码是初始化 chrome 插件后的 manifest.json 文件。是笔记应用 Binge 的 Chrome 插件的内容。

```
{
        "manifest_version": 3,
        "name": "Binge",
        "version": "1.0",
        "description": "Binge Web Clip",
        "permissions": [
                "activeTab"
        ],
        "action": {
                "default_icon": "images/icon-48.png",
                "default_title": "Binge Web Clip"
        },
        "web_accessible_resources": [
                {
                  "resources": [
                                "/images/*"
                        ],
                  "matches": [
                                "<all_urls>"
                        ]
                }
        ],
        "content_scripts": [
                {
                        "matches": [
                                "<all_urls>"
                        ],
                        "js": [
                                "scripts/content.js"
                        ],
                        "css": [
                                "css/style.css"
                        ]
                }
        ],
        "icons": {
                "16": "images/icon-16.png",
                "32": "images/icon-32.png",
                "48": "images/icon-48.png",
                "128": "images/icon-128.png"
        }
}
```

最后一段代码写于 2024 年 12 月 31 日，是多 Agent 的 AI 应用，iOS 版本的，代码就是这个项目的结构，命令行生成，不方便放出来。