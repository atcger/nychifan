#Design

##Target Clients
- Vendors
- Users 

##User Experience Design
- 注册/登陆
    - EMAIl
    - wechat
- 主页
    - 商家主页
        - 订单
             - 未来订单
             - 历史订单
        - 我的菜
             - 发布新菜
             - 更改我的菜
        - 我的状态
             - 更新状态（位置...)
             - 提醒客人
        - 我的行程（给用户看的）
             - 发布我的行程
    - 用户主页
        - 我的取餐位置（圈子）
        - 明天的菜单（菜列出商家信息）
              - 点菜
        - 如果有将来订单则默认显示将来订单：查看我的订单
              - 将来订单
                  - 菜
                  - 商家提醒信息
                  - 评价
              - 历史订单

##UI Design
```

```

##URL:RESTful
> :id number
> :name string
> :POST create/Join. For sth not exist
> :PUT update sth already exist

| Resource   | RESTful URL      | Operation | Description |
| ---------- | ---------------  | ---    | ------------- |
| Homepage   | /                | GET    | Everyone      | Homepage |
| Vendors    | /v1/vendors      | POST   | Everyone      | create a vendor |
| Vendors    | /v1/vendors      | PUT    | Vendor        | Update my profile |
| Vendors    | /v1/vendors      | DELETE | Vendor        | delete my account |
| Vendors    | /v1/vendors      | GET    | Vendor + User | View all vendors |
| Vendor     | /v1/vendor/:id   | GET    | Vendor + User | View a vendor |
| Users      | /v1/users        | POST   | Everyone      | create a user |
| Users      | /v1/users        | PUT    | User          | Update my profile | 
| Users      | /v1/users        | DELETE | User          | delete my account | 
| Users      | /v1/users        | GET    | Vendor + User | OPTIONAL: view all users | 
| User       | /v1/user/:id     | GET    | Vendor + User | View a user('s profile) | 
| Dishs      | /v1/dishes       | POST   | Vendor        | Create dish |
| Dishs      | /v1/dishes       | GET    | Vendor + User | View all dishes |
| Dish       | /v1/dish/:id     | GET    | Vendor + User | View | 
| Dish       | /v1/dish/:id     | DELETE | Vendor        | Delete (may has performance concern) | 
| Dish       | /v1/dish/:id     | PUT    | Vendor        | Update |
| Orders     | /v1/orders       | POST   | User          | Create an order |
| Orders     | /v1/orders       | GET    | Vendor + User | View all orders |
| Order      | /v1/order/:id    | GET    | Vendor + User | View |
| Order      | /v1/order/:id    | PUT    | Vendor + User | UPDATE |
| Order      | /v1/order/:id    | DELETE | Vendor + User | DELETE |
| Deliveries | /v1/deliveries   | POST   | Vendor        | Create a delivery |
| Deliveries | /v1/deliveries   | GET    | Vendor + User | View all delivery history |
| Delivery   | /v1/delivery/:id | GET    | Vendor + User | For both User and Vendor. View a delivery |
| Delivery   | /v1/delivery/:id | PUT    | Vendor + User | Update a delivery: Only for vendor |
| Delivery   | /v1/delivery/:id | DELETE | Vendor + User | Cancel a delivery: Only for vendor |

##TODO
- [ ] Mobile
- [ ] 推荐菜
- [ ] 商家促销

##Database
Postgre
