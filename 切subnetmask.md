# 切 subnetmask

去頭去尾  
前 10 後 5  
前半手動，後半 DHCP  

## /24 
### 0-255
| host ID | 用途           |
| ------- | -------------- |
| 0       | Network ID     |
| 255     | broadcast      |
| 1-10    | Server         |
| 249-254 | Network Device |
| 11-127  | fix IP         |
| 128-249 | DHCP           |

---

## /25 分兩段
### 0-127
| host ID | 用途           |
| ------- | -------------- |
| 0       | Network ID     |
| 127     | broadcast      |
| 1-10    | Server         |
| 122-126 | Network Device |
| 11-64   | fix IP         |
| 64-121  | DHCP           |

### 128-255
| host ID | 用途           |
| ------- | -------------- |
| 128     | Network ID     |
| 255     | broadcast      |
| 129-138 | Server         |
| 250-254 | Network Device |
| 139-191 | fix IP         |
| 192-249 | DHCP           |

---

## /26 分四段
### 0-63
| host ID | 用途           |
| ------- | -------------- |
| 0       | Network ID     |
| 63      | broadcast      |
| 1-10    | Server         |
| 58-62   | Network Device |
| 11-31   | fix IP         |
| 32-58   | DHCP           |

### 64-127
| host ID | 用途           |
| ------- | -------------- |
| 64      | Network ID     |
| 127     | broadcast      |
| 65-74   | Server         |
| 122-126 | Network Device |
| 75-95   | fix IP         |
| 96-122  | DHCP           |

### 128-191
| host ID | 用途           |
| ------- | -------------- |
| 128     | Network ID     |
| 191     | broadcast      |
| 129-138 | Server         |
| 186-190 | Network Device |
| 129-159 | fix IP         |
| 160-185 | DHCP           |

### 192-255
| host ID | 用途           |
| ------- | -------------- |
| 192     | Network ID     |
| 255     | broadcast      |
| 193-202 | Server         |
| 250-254 | Network Device |
| 203-223 | fix IP         |
| 224-249 | DHCP           |

---

## /27 分八段
### 0-31
| host ID | 用途           |
| ------- | -------------- |
| 0       | Network ID     |
| 31      | broadcast      |
| 1-10    | Server         |
| 26-30   | Network Device |
| 11-15   | fix IP         |
| 16-25   | DHCP           |

### 32-63
| host ID | 用途           |
| ------- | -------------- |
| 32      | Network ID     |
| 63      | broadcast      |
| 33-42   | Server         |
| 58-62   | Network Device |
| 43-47   | fix IP         |
| 48-57   | DHCP           |

### 64-95
| host ID | 用途           |
| ------- | -------------- |
| 64      | Network ID     |
| 95      | broadcast      |
| 65-74   | Server         |
| 90-94   | Network Device |
| 75-79   | fix IP         |
| 80-89   | DHCP           |

### 96-127
| host ID | 用途           |
| ------- | -------------- |
| 96      | Network ID     |
| 127     | broadcast      |
| 97-106  | Server         |
| 122-126 | Network Device |
| 107-111 | fix IP         |
| 112-121 | DHCP           |

### 128-159
| host ID | 用途           |
| ------- | -------------- |
| 128     | Network ID     |
| 159     | broadcast      |
| 129-138 | Server         |
| 154-158 | Network Device |
| 139-143 | fix IP         |
| 144-153 | DHCP           |

### 160-191
| host ID | 用途           |
| ------- | -------------- |
| 160     | Network ID     |
| 191     | broadcast      |
| 161-170 | Server         |
| 186-190 | Network Device |
| 171-175 | fix IP         |
| 176-185 | DHCP           |

### 192-223
| host ID | 用途           |
| ------- | -------------- |
| 192     | Network ID     |
| 223     | broadcast      |
| 193-202 | Server         |
| 218-222 | Network Device |
| 203-207 | fix IP         |
| 208-217 | DHCP           |

### 224-255
| host ID | 用途           |
| ------- | -------------- |
| 224     | Network ID     |
| 255     | broadcast      |
| 225-229 | Server         |
| 250-254 | Network Device |
| 230-239 | fix IP         |
| 240-249 | DHCP           |

---

後面不用再切了，太小了XD  
###### tags: `Network`
