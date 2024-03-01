# Policy Gantt Chart
Monthly policy ships each second tuesday and picks a version shipped previously up to 60d old based on non public method used to determine the best version. 

Worst case, the third monthly release has to go back to the oldest but newer z-stream
```mermaid
gantt
 title Worst case with 60d lookback for monthly
    dateFormat  YYYY-MM-DD
    section Candidate
    4.10.0  :c41000, 2024-03-01,7d
    4.10.1  :c41001, after c41000, 7d
    4.10.2  :c41002, after c41001, 7d
    4.10.3  :c41003, after c41002, 7d
    4.10.4  :c41004, after c41003, 7d
    4.10.5  :c41005, after c41004, 7d
    4.10.6  :c41006, after c41005, 7d
    4.10.7  :c41007, after c41006, 7d
    4.10.8  :c41008, after c41007, 7d
    4.10.9  :c41009, after c41008, 7d
    4.10.10 :c41010, after c41009, 7d
    4.10.11 :c41011, after c41010, 7d
    4.10.12 :c41012, after c41011, 7d
    4.10.13 :c41013, after c41012, 7d
    section Early Insights
    4.10.0  :ea41000, 2024-03-03,7d
    4.10.1  :ea41001, after ea41000, 7d
    4.10.2  :ea41002, after ea41001, 7d
    4.10.3  :ea41003, after ea41002, 7d
    4.10.4  :ea41004, after ea41003, 7d
    4.10.5  :ea41005, after ea41004, 7d
    4.10.6  :ea41006, after ea41005, 7d
    4.10.7  :ea41007, after ea41006, 7d
    4.10.8  :ea41008, after ea41007, 7d
    4.10.9  :ea41009, after ea41008, 7d
    4.10.10 :ea41010, after ea41009, 7d
    4.10.11 :ea41011, after ea41010, 7d
    4.10.12 :ea41012, after ea41011, 7d
    4.10.13 :ea41013, after ea41012, 7d
    Section Default
    4.10.0  :d41000, 2024-03-05,7d
    4.10.1  :d41001, after d41000, 7d
    4.10.2  :d41002, after d41001, 7d
    4.10.3  :d41003, after d41002, 7d
    4.10.4  :d41004, after d41003, 7d
    4.10.5  :d41005, after d41004, 7d
    4.10.6  :d41006, after d41005, 7d
    4.10.7  :d41007, after d41006, 7d
    4.10.8  :d41008, after d41007, 7d
    4.10.9  :d41009, after d41008, 7d
    4.10.10 :d41010, after d41009, 7d
    4.10.11 :d41011, after d41010, 7d
    4.10.12 :d41012, after d41011, 7d
    4.10.13 :d41013, after d41012, 7d
    Section Monthly
    4.10.1  :m41001, 2024-04-12, 30d
    4.10.5  :m41005, after m41001, 30d
    4.10.6  :m41006, after m41005, 30d
```

Best case, we select relatively current monthly versions which are approximately 14 days old at time of delivery
Candidate and Early Insights removed for brevity
```mermaid
gantt
 title Best case with 60d lookback for monthly
    dateFormat  YYYY-MM-DD
    Section Default
    4.10.0  :d41000, 2024-03-05,7d
    4.10.1  :d41001, after d41000, 7d
    4.10.2  :d41002, after d41001, 7d
    4.10.3  :d41003, after d41002, 7d
    4.10.4  :d41004, after d41003, 7d
    4.10.5  :d41005, after d41004, 7d
    4.10.6  :d41006, after d41005, 7d
    4.10.7  :d41007, after d41006, 7d
    4.10.8  :d41008, after d41007, 7d
    4.10.9  :d41009, after d41008, 7d
    4.10.10 :d41010, after d41009, 7d
    4.10.11 :d41011, after d41010, 7d
    4.10.12 :d41012, after d41011, 7d
    4.10.13 :d41013, after d41012, 7d
    Section Monthly
    4.10.1 :m41001, 2024-04-12, 30d
    4.10.5 :m41005, after m41001, 30d
    4.10.11 :m41011, after m41005, 30d
```


