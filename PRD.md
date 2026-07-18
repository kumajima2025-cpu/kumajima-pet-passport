# KumaJima Pet Passport — PRD v1.0

## 產品目標
讓熊嶼的每隻狗都有固定專屬網址，主人可查看美容紀錄；內部美容師可快速搜尋、查看注意事項、建立美容紀錄並管理儲值餘額。

## V1 核心功能
1. 寵物與飼主資料
2. 寵物搜尋
3. 寵物詳細頁
4. 新增美容紀錄
5. 儲值餘額
6. 主人專屬護照網址
7. 歷史美容紀錄
8. 美容前後照片欄位

## 角色
### 管理者／美容師
可查看與編輯所有資料、建立紀錄、更新儲值。

### 飼主
僅能透過專屬網址查看自己毛孩的公開紀錄。

## 主要畫面
- Dashboard
- 寵物列表
- 寵物詳細頁
- 新增寵物
- 新增美容紀錄
- 主人護照頁

## 資料模型
### Owner
- owner_id
- name
- phone
- line_name
- email
- note
- created_at
- active

### Pet
- pet_id
- public_code
- owner_id
- name
- breed
- gender
- birthday
- color
- weight
- allergy
- grooming_note
- balance
- cover_photo
- created_at
- active

### GroomingRecord
- record_id
- pet_id
- service_date
- groomer
- service_type
- style
- spa
- fee
- payment_method
- balance_deduction
- balance_after
- snack
- urine
- stool
- behavior
- skin
- ears
- nails
- reminder
- before_photo
- after_photo
- created_at

## V1 不做
- 線上預約
- LINE 自動通知
- 員工權限分級
- 多分店
- AI 摘要
- 自動付款

## 驗收標準
- 能建立寵物與飼主
- 每隻寵物自動產生不可猜測的 public_code
- 能新增一筆美容紀錄
- 主人頁能依 public_code 顯示該寵物資料
- 儲值扣款後餘額正確更新
- 手機畫面可正常操作
