# FIFOStockTrading

ระบบประมวลผลการซื้อขายหุ้นแบบ FIFO (First-In, First-Out) สำหรับการจัดการและวิเคราะห์ธุรกรรมการซื้อขายหุ้น

FIFO (First-In, First-Out) stock trading processing system for managing and analyzing stock trading transactions.

## คำอธิบาย (Description)

เครื่องมือนี้ใช้ในการจำลองและวิเคราะห์การซื้อขายหุ้นโดยใช้วิธี FIFO เพื่อติดตามต้นทุนและผลกำไร ช่วยให้ผู้ใช้สามารถจัดการธุรกรรมการซื้อขายหุ้นตามหลักการ FIFO และคำนวณต้นทุนได้อย่างแม่นยำ

This tool is used to simulate and analyze stock trades using the FIFO method to track costs and profits. It helps users manage stock trading transactions according to the FIFO principle and calculate costs accurately.

## คุณสมบัติ (Features)

* ประมวลผลการซื้อขายหุ้นแบบ FIFO (FIFO stock trading processing)
* ติดตามต้นทุนและผลกำไร (Track costs and profits)
* รองรับการจัดการธุรกรรมซื้อ (Buy) และขาย (Sell) (Supports Buy and Sell transaction management)
* แสดงผลข้อมูลการซื้อขายในรูปแบบ DataFrame (Displays trading data in DataFrame format)
* จัดการข้อมูลในรูปแบบ Dictionary (Manages data in Dictionary format)

## วิธีการใช้งาน (Usage)

1.  ติดตั้งไลบรารี pandas: (Install pandas library:)

    ```bash
    pip install pandas
    ```

2.  เรียกใช้ฟังก์ชัน `action_append` เพื่อเพิ่มธุรกรรมการซื้อขาย: (Call the `action_append` function to add trading transactions:)

    ```python
    import pandas as pd
    from collections import defaultdict

    def action_append(ticker, action, price, volume, df, info_dict):
        # ... (โค้ดของคุณ) ...

    ticker_df = pd.DataFrame(columns=['ticker', 'action', 'price', 'volume'])
    ticker_dict = defaultdict(list)

    ticker_df, ticker_dict = action_append('AAPL', 'B', 140, 200, ticker_df, ticker_dict)
    ticker_df, ticker_dict = action_append('MSFT', 'S', 110, 150, ticker_df, ticker_dict)

    print(ticker_df)
    print(ticker_dict)
    ```

3.  ตรวจสอบผลลัพธ์ DataFrame และ Dictionary เพื่อดูข้อมูลการซื้อขายและสถานะพอร์ตการลงทุน (Check the DataFrame and Dictionary results to view trading data and portfolio status.)

## ตัวอย่างการใช้งาน (Example Usage)

```python
# ตัวอย่างการเพิ่มธุรกรรมการซื้อขาย (Example of adding trading transactions)
ticker_df, ticker_dict = action_append('AAPL', 'B', 130, 100, ticker_df, ticker_dict)
ticker_df, ticker_dict = action_append('MSFT', 'B', 120, 200, ticker_df, ticker_dict)
ticker_df, ticker_dict = action_append('AAPL', 'S', 115, 250, ticker_df, ticker_dict)
