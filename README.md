# API

## Table of Contents
- [�����������](#c����������)
  - [*������ �����������* - branches](#������-�����������---branches)
  - [*�������������* - institutions](#�������������---institutions)
  - [*��������* - products](#��������---products)
  - [*���� ���������* - products_types](#����-���������---products_types)
  - [*����������* - suppliers](#����������---suppliers)
  - [*���� ��������� �����* - children_categories_types](#����-���������-�����---children_categories_types)
  - [*���������-�����* - children_categories](#���������-�����---children_categories)
  - [*����-���������* - price_products](#����-���������---price_products)
  - [**��������� �������* - children_day_costs](#���������-�������---children_day_costs)


## �����������:
### *������ �����������* - branches
* ���������� ������
```
  POST /api/cu_branch { "code": "0001", "name": "³��� ����� �1" }
```

* ����� �� ����, ���� ��� ���������� - ��������� ����������� ������)
```
  GET /api/branch?code=0001
```
* �������� ���� ������� � �����������
```
  GET /api/branches
```

### *�������������* - institutions
* ���������� ������
```
  POST /api/cu_institution { "code": "14", "name": "18 (���)", "prefix": "�18", "branch_code": "00000000003" }
```

* ����� �� ����, ���� ��� ���������� - ��������� ����������� ������)
```
  GET /api/institution?code=14
```
* �������� ���� ������� � �����������
```
  GET /api/institutions
```

### *��������* - products
* ���������� ������
```
  POST /api/cu_product { "code": "00000000079", "name": "���������", "products_type_code": "000000001" }
```

* ����� �� ����, ���� ��� ���������� - ��������� ����������� ������)
```
  GET /api/product?code=000000079
```
* �������� ���� ������� � �����������
```
  GET /api/products
```

### *���� ���������* - products_types
* ���������� ������
```
  POST /api/cu_products_type { "code": "000000001", "name": "������ � ������", "priority": 1 }
```

* ����� �� ����, ���� ��� ���������� - ��������� ����������� ������)
```
  GET /api/products_type?code=000000001
```
* �������� ���� ������� � �����������
```
  GET /api/products_types
```

### *����������* - suppliers
* ���������� ������
```
  POST /api/cu_supplier { "code": "25", "name": "��� ������ � 25" }
```

* ����� �� ����, ���� ��� ���������� - ��������� ����������� ������)
```
  GET /api/supplier?code=16
```
* �������� ���� ������� � �����������
```
  GET /api/suppliers
```

### *���� ��������� �����* - children_categories_types
* ���������� ������
```
  POST /api/cu_children_categories_type { "code": "00000001", "name": "���������" }
```

* ����� �� ����, ���� ��� ���������� - ��������� ����������� ������)
```
  GET /api/children_categories_type?code=16
```
* �������� ���� ������� � �����������
```
  GET /api/children_categories_types
```

### *��������� �����* - children_categories
* ���������� ������
```
  POST /api/cu_children_category { "code": "00000001", "name": "���", "children_categories_type_code": "00000001" }
```

* ����� �� ����, ���� ��� ���������� - ��������� ����������� ������)
```
  GET /api/children_category?code=000000003
```
* �������� ���� ������� � �����������
```
  GET /api/children_categories
```

### *���� ���������* - price_products
* ���������� ������
```
  POST /api/cu_price_product { "branch_code": "0003", "institution_code": "14", "product_code": "000000079  ", "price_date": "1485296673", "price": 30.25  }
```

* ����� �� ����, ���� ��� ���������� - ��������� ����������� ������)
```
  GET /api/price_product?branch_code=0003&institution_code=14&product_code=000000079&price_date=2017-01-25
```
* �������� ���� ������� � �����������
```
  GET /api/price_products
```

### *��������� �������* - children_day_costs
* ���������� ������
```
POST /api/cu_children_day_cost { "children_category_code": "000000001", "cost_date": "1485296673", "cost": 12.25 }
```

* ����� �� ����, ���� ��� ���������� - ��������� ����������� ������)
```
  GET /children_day_cost?children_category_code=000000001&cost_date=2017-01-25
```
* �������� ���� ������� � �����������
```
  GET api/children_day_costs
```
