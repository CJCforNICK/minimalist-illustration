[English](README.md)

# Minimalist Portrait Line Art

`Minimalist Portrait Line Art` 是一個 repository-local 的 Codex Skill，用來把人像、全身照、時尚穿搭照、雙人照或多人照轉換成乾淨的黑白極簡人物線稿。它的目標是在保留人物數量、姿勢、構圖、服裝輪廓與重要辨識線索的前提下，把照片中的細節重新詮釋成少量、刻意、帶有手繪感的線條。

## 專案狀態

這個 repository 現在已經可以公開分享，屬於偏早期、以文件與 skill 規格為主的專案。它包含 skill 指令、prompt 結構、品質標準與測試案例，但不包含託管服務、影像模型，或內建的人像範例素材。

## 快速開始

1. 在支援 repository-local skills 的 Codex 環境中開啟這個 repository。
2. 附上一張你有權使用的來源照片。
3. 呼叫 `$minimalist-portrait-line-art`。
4. 要求產生一張乾淨的黑白極簡線稿結果。

範例：

`Use $minimalist-portrait-line-art to turn this portrait photo into clean black-and-white minimal line art while preserving the hairstyle, face direction, expression, and clothing silhouette.`

## 這個 Skill 會做什麼

- 把輸入照片轉換成黑白極簡人物線稿
- 保留人物數量、姿勢、裁切、主要配件與重要手持物
- 預設移除原始攝影背景
- 在使用者的 ChatGPT 或 Codex 環境提供內建影像編修或生成能力時直接使用該能力
- 接受多語言請求，但內部結構化提示維持英文

## 這個 Skill 不會做什麼

- 不會託管、訓練或內建任何影像模型
- 不會建立網站、前端、後端、伺服器、資料庫或 MCP server
- 不會加入 OpenAI API 呼叫，也不需要 `OPENAI_API_KEY`
- 不會安裝 Stable Diffusion、ComfyUI、ControlNet 或其他本地模型
- 不會保證寫實等級的身分還原

## 範例流程

1. 附上來源照片。
2. 以 `$minimalist-portrait-line-art` 呼叫這個 Skill。
3. Skill 先分析人物、姿勢、裁切、服裝輪廓、配件與手持物。
4. Skill 建立結構化的英文編修提示。
5. 由宿主環境的影像工具預設產生一個結果。
6. Skill 檢查辨識度、簡化程度與禁用元素，必要時只做一次小幅定向修正。

## 主要風格特徵

- 預設為純白背景上的純黑線條
- 大致一致的中等線重
- 輕微自然的手繪感
- 選擇性斷裂輪廓
- 大片留白
- 符號化的五官
- 最多一到兩塊節制的純黑實心區域

## 使用需求

- 一個在目前任務中可用影像生成或影像編修能力的 ChatGPT 或 Codex 環境
- 使用者提供的來源照片
- 若要公開展示範例或測試，必須使用自有、已授權、已取得同意或可自由再利用的影像

不需要伺服器，不需要資料庫，也不需要本地 GPU。這個 repository 本身不包含影像模型。

## Repository-local 安裝方式

只要讓你的 Codex 環境可以存取這個 repository，就可以直接使用 `.agents/skills/minimalist-portrait-line-art/` 內的 skill。

## Personal 安裝指引

如果你想把它當成個人 skill 使用，可以把整個 skill 資料夾複製到你的個人 Codex skills 目錄，並保留以下內容：

- `SKILL.md`
- `agents/openai.yaml`
- `references/`

## 在 Codex 中使用

請用 `$minimalist-portrait-line-art` 明確呼叫這個 skill。

範例：

`Use $minimalist-portrait-line-art to turn this portrait photo into clean black-and-white minimal line art.`

## 使用範例

- `Use $minimalist-portrait-line-art to turn this portrait photo into clean black-and-white minimal line art.`
- `使用 $minimalist-portrait-line-art，保留兩個人的身高差、姿勢和服裝輪廓，移除背景。`
- `使用 $minimalist-portrait-line-art，使用透明背景，並保留人物手中的花束。`
- `使用 $minimalist-portrait-line-art，把這張人物照片轉換成黑白極簡人物線稿。`

## 專案結構

```text
.agents/
  skills/
    minimalist-portrait-line-art/
      SKILL.md
      agents/openai.yaml
      references/
        style-guide.md
        prompt-recipes.md
        quality-checklist.md
tests/
  test-cases.md
README.md
README.zh-TW.md
.gitignore
```

## 測試方式

目前 repository 使用文字型測試計畫，放在 [tests/test-cases.md](tests/test-cases.md)。測試涵蓋單人、雙人、多人、穿搭、配件、透明背景與修正流程，也包含英文與繁體中文的觸發範例。不要用私人或未授權照片直接執行這些測試。

## 隱私指引

- 不要提交私人肖像照片
- 不要把私人肖像上傳到公開的 issue、pull request 或示範資料夾
- 不要把使用者上傳照片存進 skill
- 若要公開可辨識人物照片，請先取得當事人同意
- 不要把參考照片嵌成 base64 內容

## 著作權指引

- 不要公開受版權保護的風格參考書頁
- 不要重製拍攝到的書頁文字或圖像
- 應把觀察整理成抽象的文字風格規則
- 公開範例只能使用自有、已授權或可自由再利用的影像

## 成本與基礎設施

這個 repository 不會替使用者支付、代理或代管影像生成。實際生成能力取決於使用者自己的 ChatGPT 或 Codex 環境，可用量也可能計入使用者自己的方案或圖片生成額度。此專案不引入持續性的基礎設施成本。

## 公開分享前檢查

在把這個 repository 對外分享前，請再確認：

- 沒有提交任何私人肖像照片
- 沒有把受版權保護的參考頁面複製進 repository
- 公開範例都使用自有、已授權或可自由再利用的影像
- 你可以接受目前「尚未決定授權條款」的公開狀態

## 目前限制

- 輸出品質取決於宿主環境的影像編修能力
- 某些宿主環境可能只能生成，不能穩定保留人物身分與姿勢
- 複雜多人場景可能需要再經過一次由使用者同意的額外迭代
- 透明背景是否可用取決於目前宿主工具

## 路線圖

- 強化多人姿勢較複雜時的 prompt recipe
- 改善保留單一指定環境物件的指引
- 補充更多透明背景輸出的驗收範例

## 貢獻方式

請讓這個 skill 維持在單一明確任務上，保留 progressive disclosure，不要加入 API fallback，也不要加入會改變成本模型的基礎設施。新增範例或測試時，請只使用已取得同意、自有、已授權或可自由再利用的影像。

## 授權狀態

正式公開前會再決定授權條款。不要自行猜測或填入著作權擁有者名稱。
