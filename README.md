# End to End Analytics and ML on Olist: Customer, Seller and Logistics Intelligence
![Dashboard](https://github.com/ShaikhBorhanUddin/End-to-End-Analytics-and-ML-on-Olist-Customer-Seller-and-Logistics-Intelligence/blob/main/Images/olist_banner.png?raw=true) 

🔹 1. Predict Customer Lifetime Value (CLV)

Why it matters: Businesses want to know which customers are worth investing in (discounts, loyalty programs, retention campaigns).

Target: Total revenue from a customer over their entire observed history (regression).

Features (SQL aggregates):

Number of orders placed

Average order value

Average review score

Customer’s region/state

Time since first purchase

🔹 2. Predict Payment Method Choice

Why it matters: Helps optimize checkout flow, fraud prevention, and financial planning.

Target: payment_type (credit card, boleto, voucher, debit card, etc.).

Features (SQL joins):

Total order value

Number of installments (if applicable)

Customer state

Product category mix in the order

🔹 3. Estimate Shipping Cost (Freight Value Prediction)

Why it matters: Olist pays attention to freight costs — predicting them can help set better shipping fees and optimize logistics.

Target: freight_value (continuous, regression).

Features (SQL joins):

Order weight & volume (from product dimensions)

Distance proxy (seller_state vs customer_state)

Number of items in order

Delivery time window

🔹 4. Predict Customer Review Sentiment (Positive/Negative)

Why it matters: Monitoring customer satisfaction and flagging potential complaints.

Target: Binary sentiment (e.g., review_score ≥ 4 = positive, ≤ 2 = negative).

Features (SQL joins):

Delivery delays

Number of items in order

Product category

Seller past performance (avg review score)

(Bonus: you could even use NLP on review_comment_message, combining SQL + ML + NLP).

🔹 5. Predict Product Return / Refund Likelihood

Why it matters: Returns are costly. Being able to anticipate them helps with stock management, fraud detection, and logistics.

Target: Whether a payment was refunded (from order_status = canceled or refunded orders).

Features (SQL joins):

Product category

Order value

Delivery time

Customer history (first order vs repeat buyer)
