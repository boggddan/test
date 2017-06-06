# API

## Table of Contents
- [Справочники](#cправочники)
  - [*Отделы образования* - branches](#Отделы-образования---branches)
  - [*Подразделения* - institutions](#Подразделения---institutions)
  - [*Продукты* - products](#Продукты---products)
  - [*Типы продуктов* - products_types](#Типы-продуктов---products_types)
  - [*Поставщики* - suppliers](#Поставщики---suppliers)
  - [*Типы категорий детей* - children_categories_types](#Типы-категорий-детей---children_categories_types)
  - [*Категорий-детей* - children_categories](#Категорий-детей---children_categories)
  - [*Цены-продуктов* - price_products](#Цены-продуктов---price_products)
  - [**Стоимость детодня* - children_day_costs](#Стоимость-детодня---children_day_costs)


## Справочники:
### *Отделы образования* - branches
* Добавление записи
```
  POST /api/cu_branch { "code": "0001", "name": "Відділ освіти №1" }
```

* Поиск по коду, если нет параметров - последняя добавленная запись)
```
  GET /api/branch?code=0001
```
* Просмотр всех записей в справочнике
```
  GET /api/branches
```

### *Подразделения* - institutions
* Добавление записи
```
  POST /api/cu_institution { "code": "14", "name": "18 (ДОУ)", "prefix": "Д18", "branch_code": "00000000003" }
```

* Поиск по коду, если нет параметров - последняя добавленная запись)
```
  GET /api/institution?code=14
```
* Просмотр всех записей в справочнике
```
  GET /api/institutions
```

### *Продукты* - products
* Добавление записи
```
  POST /api/cu_product { "code": "00000000079", "name": "Баклажани", "products_type_code": "000000001" }
```

* Поиск по коду, если нет параметров - последняя добавленная запись)
```
  GET /api/product?code=000000079
```
* Просмотр всех записей в справочнике
```
  GET /api/products
```

### *Типы продуктов* - products_types
* Добавление записи
```
  POST /api/cu_products_type { "code": "000000001", "name": "Вироби з молока", "priority": 1 }
```

* Поиск по коду, если нет параметров - последняя добавленная запись)
```
  GET /api/products_type?code=000000001
```
* Просмотр всех записей в справочнике
```
  GET /api/products_types
```

### *Поставщики* - suppliers
* Добавление записи
```
  POST /api/cu_supplier { "code": "25", "name": "ТОВ Постач № 25" }
```

* Поиск по коду, если нет параметров - последняя добавленная запись)
```
  GET /api/supplier?code=16
```
* Просмотр всех записей в справочнике
```
  GET /api/suppliers
```

### *Типы категорий детей* - children_categories_types
* Добавление записи
```
  POST /api/cu_children_categories_type { "code": "00000001", "name": "Дошкільний" }
```

* Поиск по коду, если нет параметров - последняя добавленная запись)
```
  GET /api/children_categories_type?code=16
```
* Просмотр всех записей в справочнике
```
  GET /api/children_categories_types
```

### *Категорий детей* - children_categories
* Добавление записи
```
  POST /api/cu_children_category { "code": "00000001", "name": "Яслі", "children_categories_type_code": "00000001" }
```

* Поиск по коду, если нет параметров - последняя добавленная запись)
```
  GET /api/children_category?code=000000003
```
* Просмотр всех записей в справочнике
```
  GET /api/children_categories
```

### *Цены продуктов* - price_products
* Добавление записи
```
  POST /api/cu_price_product { "branch_code": "0003", "institution_code": "14", "product_code": "000000079  ", "price_date": "1485296673", "price": 30.25  }
```

* Поиск по коду, если нет параметров - последняя добавленная запись)
```
  GET /api/price_product?branch_code=0003&institution_code=14&product_code=000000079&price_date=2017-01-25
```
* Просмотр всех записей в справочнике
```
  GET /api/price_products
```

### *Стоимость детодня* - children_day_costs
* Добавление записи
```
POST /api/cu_children_day_cost { "children_category_code": "000000001", "cost_date": "1485296673", "cost": 12.25 }
```

* Поиск по коду, если нет параметров - последняя добавленная запись)
```
  GET /children_day_cost?children_category_code=000000001&cost_date=2017-01-25
```
* Просмотр всех записей в справочнике
```
  GET api/children_day_costs
```
