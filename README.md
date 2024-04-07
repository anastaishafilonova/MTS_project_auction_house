# MTS_project_auction_house
## Проект "Аукционный дом". Java, 2 семестр.  
### Команда: Лебедева Мария, Филонова Анастасия, Шаров Святослав.  
## Микросервисы:  
### 1. ItemService
Сущности:  
`Customer`\ - класс покупателя, имеет следующие поля: _customer_id_, _first_name_, _last_name_, _balance_ (сколько денег на счету), _goods_ (список купленных товаров), _bet_ (текущая ставка)  
`Good`\ - класс товара, имеет следующие поля: _good_id_, _name_, _price_, _owner_ (тот, кто купил), _seller_ (тот, кто продаёт), _start_time_ (время выставления на продажу)  
`Seller`\ - класс продавца, имеет следующие поля: __seller_id_, __first_name_, _last_name_, _balance_ (сколько денег на счету), _goods_ (cписок продаваемых товаров)  
Для каждой сущности должны быть созданы отдельные репозитории: `CustomerRepository`\, `GoodRepository`\, `SellerRepository`\.    
Все методы взаимодействия с сущностями прописываются в сервисах:  
`CustomerService`\: createCustomer, deleteCustomer, updateCustomer, getCustomer, getBalance (по _customer_id_), increaseBalance (по _customer_id_ на какую-то конкретную сумму), decreaseBalance (по _customer_id_ на какую-то конкретную сумму), buyGood, deleteGood, increaseBet (по _customer_id_ на какую-то конкретную сумму)  
