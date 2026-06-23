# Repository 架構說明

本文件說明本 Repository 各資料夾之用途與內容規劃。

## preprocessing/

存放資料前處理相關程式與說明文件，包括原始資料整理、資料清理、特徵工程、病患層級資料切分、滑動視窗建立與模型資料集生成。

## phase1_adjustment_detection/

存放 Phase 1 模型相關內容。此階段任務為判斷病患目前是否需要進行呼吸器參數調整。

主要內容包含：

```text
lstm/
gru/
fixed_baseline/
bayesian_optimization/
best_model/
evaluation/
shap/
```

## phase2_1_direction_classification/

存放 Phase 2-1 模型相關內容。此階段任務為預測呼吸器參數之調整方向，包括調高、維持或調低。

## phase2_2_parameter_regression/

存放 Phase 2-2 模型相關內容。此階段任務為預測呼吸器參數之建議調整幅度。

## figures/

存放論文與 Repository 說明使用之圖片，包括研究流程圖、模型架構圖、結果圖與可解釋性分析圖。

## results/

存放整理後之模型結果摘要，例如交叉驗證結果、測試集結果、最佳模型比較與論文表格資料。

本資料夾不存放原始資料、大型訓練紀錄或模型權重檔。

## docs/

存放 Repository 說明文件、研究歷程、實驗紀錄與論文進度整理。

## thesis/

存放與碩士論文撰寫相關之整理內容，例如章節摘要、表格草稿與圖表說明。
