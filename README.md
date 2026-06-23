# 呼吸器調整建議深度學習模型

## 專案簡介

本 Repository 為碩士論文研究之公開整理版本，內容包含呼吸器調整建議模型之研究架構、資料前處理流程、模型訓練設計、實驗結果整理與相關文件。

本研究以重症加護病房侵入式機械通氣患者之時間序列資料為基礎，建立呼吸器調整相關預測模型。整體研究流程包含資料前處理、病患層級資料切分、時間序列樣本建立、模型訓練、超參數最佳化、模型評估與可解釋性分析。

本 Repository 不包含任何病患原始資料、可識別資料、模型權重檔或大型訓練紀錄。

## 研究架構

本研究分為三個主要任務。

### Phase 1：呼吸器是否需要調整

建立二元分類模型，用以判斷目前病患是否需要進行呼吸器參數調整。

### Phase 2-1：呼吸器調整方向分類

建立多類別分類模型，用以預測呼吸器參數之調整方向，包括調高、維持或調低。

### Phase 2-2：呼吸器參數調整量預測

建立回歸模型，用以預測呼吸器參數之建議調整幅度。

## 使用模型與方法

本研究主要使用 Long Short-Term Memory（LSTM）與 Gated Recurrent Unit（GRU）模型，並透過 Bayesian Optimization 進行超參數最佳化。模型評估採用病患層級資料切分，以降低同一病患資料同時出現在訓練集與測試集所造成的資料洩漏風險。

此外，本研究亦使用 SHAP（SHapley Additive exPlanations）進行模型可解釋性分析，以了解不同輸入特徵對模型預測結果之影響。

## Repository 架構

詳細資料夾說明請參閱：

```text
docs/repository_structure.md
```

主要資料夾如下：

```text
preprocessing/
phase1_adjustment_detection/
phase2_1_direction_classification/
phase2_2_parameter_regression/
figures/
results/
docs/
thesis/
```

## 目前進度

```text
資料前處理：已完成
Phase 1：已完成
Phase 2-1：已完成
Phase 2-2：進行中
論文撰寫：進行中
```

## 使用限制

本 Repository 僅作為學術研究成果整理與展示用途。未經作者書面同意，不得複製、散布、修改、商業使用或以任何形式重新發表本 Repository 內之程式碼、文件與研究成果。

如需引用或使用本研究內容，請先與作者聯絡。

## 作者

本 Repository 用於碩士論文研究成果之版本管理與公開展示。
