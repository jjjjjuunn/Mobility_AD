# 🎯 CIFAR-100 Image Classification Project

CIFAR-100 데이터셋을 사용한 이미지 분류 프로젝트

## 📊 최종 결과

| Method | Val Acc | Test Acc | Improvement |
|--------|---------|----------|-------------|
| Baseline | 41.85% | 41.57% | - |
| **Our Model** | **47.97%** | **49.18%** | **+7.61%** ✅ |

## 🚀 주요 기술

### 1. Data Augmentation
- RandomCrop(32, padding=4)
- RandomHorizontalFlip(p=0.5)
- CIFAR-100 표준 Normalization

### 2. 모델 구조
```python
- Conv1: 3 → 32 filters (3x3)
- Conv2: 32 → 64 filters (3x3)
- Conv3: 64 → 128 filters (3x3)
- Batch Normalization (각 Conv 후)
- Dropout(0.3)
- FC1: 2048 → 256
- FC2: 256 → 100