# Hypothetical 4.15 rollout with Policies
Monthly policy ships each second tuesday and picks a version shipped previously up to 60d old based on non public method used to determine the best version. 
48hr delay between Candidate, Early Insights, and Default respectively

First, Candidate, Early Insights, and Default channels only
```mermaid
gantt
    dateFormat  YYYY-MM-DD
    section Candidate
    4.15.0-rc.0 :c415rc0, 2023-12-12, 7d
    4.15.0-rc.1 :c415rc1, 2024-01-05, 7d
    4.15.0-rc.2 :c415rc2, 2024-01-12, 7d
    4.15.0-rc.3 :c415rc3, 2024-01-19, 7d
    4.15.0-rc.4 :c415rc4, 2024-01-26, 7d
    4.15.0-rc.5 :c415rc5, 2024-02-02, 7d
    4.15.0-rc.7 :c415rc7, 2024-02-14, 7d
    4.15.0-rc.8 :c415rc8, 2024-02-21, 7d
    4.15.0  :c41500, 2024-03-01,7d
    4.15.1  :c41501, after c41500, 7d
    4.15.2  :c41502, after c41501, 7d
    4.15.3  :c41503, after c41502, 7d
    4.15.4  :c41504, after c41503, 7d
    4.15.5  :c41505, after c41504, 7d
    4.15.6  :c41506, after c41505, 7d
    4.15.7  :c41507, after c41506, 7d
    4.15.8  :c41508, after c41507, 7d
    4.15.9  :c41509, after c41508, 7d
    4.15.10 :c41510, after c41509, 7d
    4.15.11 :c41511, after c41510, 7d
    4.15.12 :c41512, after c41511, 7d
    4.15.13 :c41513, after c41512, 7d
    section Early Insights
    4.15.0  :ea41500, 2024-03-03,7d
    4.15.1  :ea41501, after ea41500, 7d
    4.15.2  :ea41502, after ea41501, 7d
    4.15.3  :ea41503, after ea41502, 7d
    4.15.4  :ea41504, after ea41503, 7d
    4.15.5  :ea41505, after ea41504, 7d
    4.15.6  :ea41506, after ea41505, 7d
    4.15.7  :ea41507, after ea41506, 7d
    4.15.8  :ea41508, after ea41507, 7d
    4.15.9  :ea41509, after ea41508, 7d
    4.15.10 :ea41510, after ea41509, 7d
    4.15.11 :ea41511, after ea41510, 7d
    4.15.12 :ea41512, after ea41511, 7d
    4.15.13 :ea41513, after ea41512, 7d
    Section Default
    4.15.0  :d41500, 2024-03-05,7d
    4.15.1  :d41501, after d41500, 7d
    4.15.2  :d41502, after d41501, 7d
    4.15.3  :d41503, after d41502, 7d
    4.15.4  :d41504, after d41503, 7d
    4.15.5  :d41505, after d41504, 7d
    4.15.6  :d41506, after d41505, 7d
    4.15.7  :d41507, after d41506, 7d
    4.15.8  :d41508, after d41507, 7d
    4.15.9  :d41509, after d41508, 7d
    4.15.10 :d41510, after d41509, 7d
    4.15.11 :d41511, after d41510, 7d
    4.15.12 :d41512, after d41511, 7d
    4.15.13 :d41513, after d41512, 7d
```

Best case, we select relatively current monthly versions which are approximately 14 days old at time of delivery
Candidate and Early Insights removed for brevity
```mermaid
gantt
    dateFormat  YYYY-MM-DD
    Section Default
    4.15.0  :d41500, 2024-03-05,7d
    4.15.1  :d41501, after d41500, 7d
    4.15.2  :d41502, after d41501, 7d
    4.15.3  :d41503, after d41502, 7d
    4.15.4  :d41504, after d41503, 7d
    4.15.5  :d41505, after d41504, 7d
    4.15.6  :d41506, after d41505, 7d
    4.15.7  :d41507, after d41506, 7d
    4.15.8  :d41508, after d41507, 7d
    4.15.9  :d41509, after d41508, 7d
    4.15.10 :d41510, after d41509, 7d
    4.15.11 :d41511, after d41510, 7d
    4.15.12 :d41512, after d41511, 7d
    4.15.13 :d41513, after d41512, 7d
    Section Monthly
    4.15.1 :m41501, 2024-04-12, 30d
    4.15.5 :m41505, after m41501, 30d
    4.15.11 :m41511, after m41505, 30d
```

Now, worst case, 4.15.6 is the third monthly release and it's as old as possible given 60d lookback
Candidate and Early Insights removed for brevity
```mermaid
gantt
    dateFormat  YYYY-MM-DD
    Section Default
    4.15.0  :d41500, 2024-03-05,7d
    4.15.1  :d41501, after d41500, 7d
    4.15.2  :d41502, after d41501, 7d
    4.15.3  :d41503, after d41502, 7d
    4.15.4  :d41504, after d41503, 7d
    4.15.5  :d41505, after d41504, 7d
    4.15.6  :d41506, after d41505, 7d
    4.15.7  :d41507, after d41506, 7d
    4.15.8  :d41508, after d41507, 7d
    4.15.9  :d41509, after d41508, 7d
    4.15.10 :d41510, after d41509, 7d
    4.15.11 :d41511, after d41510, 7d
    4.15.12 :d41512, after d41511, 7d
    4.15.13 :d41513, after d41512, 7d
    Section Monthly
    4.15.1  :m41501, 2024-04-12, 30d
    4.15.5  :m41505, after m41501, 30d
    4.15.6  :m41506, after m41505, 30d
```


