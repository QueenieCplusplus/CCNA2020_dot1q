# CCNA2020_dot1q
IEEE 802.1q defines VLAN tag

# 802.1Q

允許多個網橋 Network Bridge 在資料不外洩的情況下共用同一個實體網路。
等同允許多個 VLAN 藉由 Switcher 連接在一起。

# 802.1q header

為原始影格 frame 多加入 802.1q header 欄位，此標頭含有四個欄位，最主要是 TPID 與 VID。

# VLAN 架構

是 IT 部門為企業的內部實體網路再切出個別獨立的邏輯網路端。

# VLAN 標籤

原理是 edge switch 幫 frame 標記適當的 vlan id，該 frame 傳送到部門下相對應的設備下則該標識會被移除。

能幫助影格在傳送過程中（廣播）, 不會被其他不相干的部門設備嗅探。

且可使多個 VLAN 用一個連接多路復用。

# Trunk Port

此阜是用於 Switcher 與 Switcher 之間溝通 VLAN 的介面。

設定方式：


             int Gi0/12
             switchport mode trunk


設定到主機的方式：


             int Gi0/1
             switchport mode access
             switchport access vlan234

# Switch port ( access port )

交換器原則上是一個阜配置一個 VLAN， 同一 VLAN 上的所有終端裝置共享同一廣播網域 Broadcast Domain。
