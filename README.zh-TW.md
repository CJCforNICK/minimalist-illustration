[English](README.md)

# Minimalist Portrait Line Art

`Minimalist Portrait Line Art` 是一個 repository-local 的 Codex Skill，用來把人像、全身照、穿搭照、雙人照、多人合照，以及動作姿態照片轉換成乾淨的黑白極簡人物線條畫。

這個 Skill 不是照片描邊濾鏡。它的核心是把照片重新整理成一張稀疏的符號化插畫：先保留姿勢、構圖、手勢、服裝輪廓、臉部方向與重要辨識線索，再捨棄攝影細節，讓成品看起來簡單、可讀、帶有手繪感。

## 專案狀態

這個 repository 目前可以公開分享，屬於早期、以文件與 skill 規格為主的專案。它包含 skill 指令、prompt 結構、品質標準與文字型測試案例，但不包含託管服務、影像模型、API 腳本，或內建的人像範例素材。

目前重點是打磨極簡人物重建的 prompt 與驗收邏輯，特別是多人手部關係、壓縮姿勢、臉部遮擋，以及近景手勢這些容易失控的案例。

## 快速開始

1. 在支援 repository-local skills 的 Codex 環境中開啟這個 repository。
2. 附上一張你有權使用的來源照片。
3. 呼叫 `$minimalist-portrait-line-art`。
4. 要求產生一張乾淨的黑白極簡線條畫結果。

範例：

`Use $minimalist-portrait-line-art to turn this photo into sparse black-and-white minimalist line art while preserving the pose, face direction, clothing silhouette, and hand gesture.`

## 核心方法

這個 Skill 會把照片視為「結構」，而不是要逐一保留的表面細節。

- 生成前先建立 `Pose Map`。
- 再把 `Pose Map` 轉成 `Drawing Plan`。
- 保留姿態、視線、手部歸屬、物件歸屬、服裝層次與重要遮擋。
- 用符號化標記處理臉和手，而不是寫實解剖。
- 移除背景、陰影、材質、可讀文字、密集皺摺與攝影式立體感。

因此，理想結果應該更像極簡生活感塗鴉或 editorial line figure，而不是精緻肖像線稿。

## 這個 Skill 會做什麼

- 把輸入照片轉換成黑白極簡人物線條畫。
- 保留人物數量、相對位置、姿勢、裁切、主要配件與重要手持物。
- 在雙人或多人照片中，優先保留手勢、接觸關係與物件歸屬。
- 在蹲姿、坐姿、滑板等壓縮或動作姿勢中，保留身體壓縮、支撐點、膝蓋彎曲、腳的位置與遮擋關係。
- 準確保留臉部可見度：如果原圖的臉被帽簷、頭髮、墨鏡、口罩、角度、動作、物件或裁切遮住，成品不應該補出完整臉。
- 預設移除原始攝影背景。
- 在使用者的 ChatGPT 或 Codex 環境提供內建影像編修或生成能力時，直接使用該能力。
- 接受多語言請求，但結構化 image prompt 維持英文。

## 這個 Skill 不會做什麼

- 不會託管、訓練或內建任何影像模型。
- 不會建立網站、後端、伺服器、資料庫或 MCP server。
- 不會加入 OpenAI API 呼叫，也不需要 `OPENAI_API_KEY`。
- 不會安裝 Stable Diffusion、ComfyUI、ControlNet 或其他本地模型。
- 不會保證寫實等級的身份還原。
- 不會把使用者上傳的人像照片存進 repository。

## 範例流程

1. 附上來源照片。
2. 以 `$minimalist-portrait-line-art` 呼叫這個 Skill。
3. Skill 檢查照片中必須保留的視覺特徵。
4. Skill 建立 `Pose Map`，包含臉部可見度、手的位置、手持物、支撐點與遮擋關係。
5. Skill 建立 `Drawing Plan`，包含黑色塊面、主要輪廓、層次分隔、臉部符號與刻意省略項目。
6. 宿主環境的影像工具預設產生一張結果。
7. Skill 檢查姿勢準確度、辨識度、簡化程度與禁用元素。
8. 必要時只做一次窄範圍修正，例如降低臉部寫實度或恢復被遮住的臉。

## 主要風格特徵

- 預設為純白背景上的純黑線條。
- 大致一致的中等線重。
- 輕微自然的手繪感。
- 選擇性斷裂輪廓，而不是完整閉合描邊。
- 大片留白。
- 由點、短線、小弧線構成的符號化五官。
- 保留手勢但省略解剖細節的簡化手部。
- 只保留必要衣領、下襬、袖口、腰線、口袋、背帶或服裝層次分隔。
- 最多一到兩塊節制的純黑實心區域。

## 重要繪畫規則

- 從姿勢計畫重建人物，不要沿著照片每條邊緣描線。
- 先保留身體結構，再加入風格標記。
- 黑色塊面是平面構圖錨點，不是陰影。
- 如果原圖的臉幾乎看不到，就讓成品也幾乎看不到臉。
- 如果手、腳或肢體不清楚，應該簡化或藏進輪廓，不要發明解剖細節。
- 如果服裝層次混在一起，只加最少的邊界線讓它可讀。
- 如果結果像是被清理過的寫實線稿，應該回到 `Drawing Plan` 重建，而不是繼續修補。

## 使用需求

- 一個在目前任務中可用影像生成或影像編修能力的 ChatGPT 或 Codex 環境。
- 使用者提供的來源照片。
- 若要公開展示範例或測試，必須使用自有、已授權、已取得同意或可自由再利用的影像。

不需要伺服器，不需要資料庫，也不需要本地 GPU。這個 repository 本身不包含影像模型。

## Repository-Local 安裝方式

只要讓你的 Codex 環境可以存取這個 repository，就可以直接使用 `.agents/skills/minimalist-portrait-line-art/` 內的 skill。

## Personal 安裝指引

如果你想把它當成個人 skill 使用，可以把整個 skill 資料夾複製到你的個人 Codex skills 目錄，並保留以下內容：

- `SKILL.md`
- `agents/openai.yaml`
- `references/`

## 在 Codex 中使用

請用 `$minimalist-portrait-line-art` 明確呼叫這個 skill。

範例：

- `Use $minimalist-portrait-line-art to turn this portrait photo into clean black-and-white minimal line art.`
- `使用 $minimalist-portrait-line-art，保留兩個人的身高差、姿勢和服裝輪廓，移除背景。`
- `使用 $minimalist-portrait-line-art，保留帽簷遮住臉的狀態，不要補出完整五官。`
- `使用 $minimalist-portrait-line-art，保留蹲姿滑板動作，並簡化臉、手、鞋子與衣服皺褶。`

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

目前 repository 使用文字型測試計畫，放在 [tests/test-cases.md](tests/test-cases.md)。測試涵蓋單人、雙人、多人、穿搭、配件、透明背景、修正流程、臉部遮擋與壓縮姿勢案例。不要用私人或未授權照片直接執行這些測試。

## 隱私指引

- 不要提交私人肖像照片。
- 不要把私人肖像上傳到公開的 issue、pull request 或示範資料夾。
- 不要把使用者上傳照片存進 skill。
- 若要公開可辨識人物照片，請先取得當事人同意。
- 不要把參考照片嵌成 base64 內容。

## 著作權指引

- 不要公開受版權保護的風格參考書頁。
- 不要重製拍攝到的書頁文字或圖像。
- 應把觀察整理成抽象的文字風格規則。
- 公開範例只能使用自有、已授權或可自由再利用的影像。

## 成本與基礎設施

這個 repository 不會替使用者支付、代理或代管影像生成。實際生成能力取決於使用者自己的 ChatGPT 或 Codex 環境，可用量也可能計入使用者自己的方案或圖片生成額度。此專案不引入持續性的基礎設施成本。

## 公開分享前檢查

在把這個 repository 對外分享前，請再確認：

- 沒有提交任何私人肖像照片。
- 沒有把受版權保護的參考頁面複製進 repository。
- 公開範例都使用自有、已授權或可自由再利用的影像。
- 你可以接受目前「尚未決定授權條款」的公開狀態。

## 目前限制

- 輸出品質取決於宿主環境的影像編修能力。
- 某些宿主環境可能只能生成，不能穩定保留人物身份與姿勢。
- 複雜多人場景可能需要再經過一次由使用者同意的額外迭代。
- 強烈近景透視與手勢仍可能需要定向修正。
- 透明背景是否可用取決於目前宿主工具。

## 路線圖

- 補充更多壓縮姿勢、動作姿勢與遮擋臉的文字測試。
- 改善近景手勢的規則，避免過度描繪手部解剖。
- 改善保留單一指定環境支撐物的指引，例如椅子、路緣或車頂。
- 補充更多透明背景輸出的驗收範例。

## 貢獻方式

請讓這個 skill 維持在單一明確任務上，保留 progressive disclosure，不要加入 API fallback，也不要加入會改變成本模型的基礎設施。新增範例或測試時，請只使用已取得同意、自有、已授權或可自由再利用的影像。

## 授權狀態

正式公開前會再決定授權條款。不要自行猜測或填入著作權擁有者名稱。
