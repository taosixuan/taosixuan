select DELIVERED_UPC, delivered_date_pt, sum(FINAL_CHARGE_AMT_USD) as FINAL_CHARGE_AMT_USD, sum(PICKED_QUANTITY) as PICKED_QUANTITY , count(distinct order_delivery_id) as order_delivery_id, count(distinct user_id) as user_id, sum(FINAL_CHARGE_AMT_USD)/count(distinct user_id) as Spend_Per_Customer, sum(PICKED_QUANTITY)/count(distinct user_id) as Units_Per_Customer, count(distinct order_delivery_id)/count(distinct user_id) as Deliveries_Per_Customer,
sum(FINAL_CHARGE_AMT_USD)/count(distinct order_delivery_id) as Spend_Per_Delivery,
sum(PICKED_QUANTITY)/count(distinct order_delivery_id) as Units_Per_Delivery
from vw_explore_order_items_refactored          
group by 1,2
order by 2
