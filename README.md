# API

## ����
- [��������](#��������)
  - [*��������* - branches](#��������---branches)
  - [*ϳ�������* - institutions](#ϳ�������---institutions)
  - [*�������� ����������* - products](#�������� ����������---products)
  - [*���� �������� ����������* - products_types](# ����-��������-����������---products_types)
  - [*��������* - packages](#��������---packages)
  - [*�������� �������������* - suppliers_packages](#��������-�������������---suppliers_packages)
  - [*�������������* - suppliers](# �������������---suppliers)
  - [*ֳ�� �� ��������* - price_products](#ֳ��-��-��������---price_products)
  - [*������� ������� ������* - children_day_costs](#�������-�������-������---children_day_costs)
  - [*������� ������ ��������* - causes_deviations](#�������-������-��������---causes_deviations)
  - [*ĳ��* - children](#ĳ��---children)
  - [*������� ����* - children_categories](#�������-����---children_categories)
  - [*����� ����* - children_groups](#����� ����---children_groups)
  - [*���� ������� ����* - children_categories_types](#����-�������-����---children_categories_types)
  - [*������� ��������� ������* - reasons_absences](#�������-���������-������---reasons_absences)
- [���������](#���������)
  - [*���������� �������������* - supplier_orders](#����������-�������������---supplier_orders)
  - [*����������� ���* - receipts](#�����������-���---receipts)
  - [*���������� �������� ����������* - institution_orders](#����������-��������-����������---institution_orders)
  - [*������������ ���������� �������� ����������* - io_corrections](#������������-����������-��������-����������---io_corrections)
  - [*����-������* - menu_requirements](#����-������---menu_requirements)
  - [*������* - timesheets](#������---timesheets)

### ��������
### *��������* - branches
```
  POST /api/cu_institution { "code": "14", "name": "18 (���)", "prefix": "�18", "branch_code": "00000000003" }
  GET /api/institution?code=14
  GET /api/institutions
```

### *ϳ�������* - institutions
```
  POST /api/cu_institution { "code": "14", "name": "18 (���)", "prefix": "�18", "branch_code": "00000000003" }
  GET /api/institution?code=14
  GET /api/institutions

```

### *�������� ����������* - products
```
  POST /api/cu_product { "code": "00000000079", "name": "���������", "products_type_code": "000000001" }
  GET /api/product?code=000000079
  GET /api/products
```

### *���� �������� ����������* - products_types
```
  POST /api/cu_products_type { "code": "000000001", "name": "������ � ������", "priority": 1 }
  GET /api/products_type?code=000000001
  GET /api/products_types
```

### *��������* - packages
```
  POST /api/cu_package { "code": "000000001", "name": "ѳ��� 5 ��", "conversion_factor": 5.000000 }
  GET /api/package?code=000000001
  GET /api/packages
```

### *�������� �������������* - suppliers_packages
```
  POST /api/cu_suppliers_package { "institution_code": "14", "supplier_code": "8", "product_code": "00000000079", "package_code": "000000001", "period": "1496448000", "activity": 1 }
  GET /api/suppliers_package?institution_code=14&supplier_code=8&product_code=00000000079&package_code=000000001&period=2017-05-03
  GET /api/suppliers_packages
```

### *�������������* - suppliers
```
  POST /api/cu_supplier { "code": "25", "name": "��� ������ � 25" }
  GET /api/supplier?code=16
  GET /api/suppliers

```

### *ֳ�� �� ��������* - price_products
```
  POST /api/cu_price_product { "branch_code": "0003", "institution_code": "14", "product_code": "000000079  ", "price_date": "1485296673", "price": 30.25  }
  GET /api/price_product?branch_code=0003&institution_code=14&product_code=000000079&price_date=2017-01-25
  GET /api/price_products

```

### *������� ������� ������* - children_day_costs
```
  POST /api/cu_children_day_cost { "children_category_code": "000000001", "cost_date": "1485296673", "cost": 12.25 }
  GET /children_day_cost?children_category_code=000000001&cost_date=2017-01-25
  GET api/children_day_costs

```

### *������� ������ ��������* - causes_deviations
```
  POST /api/cu_causes_deviation { "code": "000000002", "name": "������� 2" }
  GET /api/causes_deviation?code=000000002
  GET /api/causes_deviations
```

### *ĳ��* - children
```
  POST /api/cu_child { "code": "000000001", "name": "������ ���� ��������" }
  GET /api/child?code=000000001
  GET /api/children
```

### *������� ����* - children_categories
```
  POST /api/cu_children_category { "code": "00000001", "name": "���", "children_categories_type_code": "00000001" }
  GET /api/children_category?code=000000003
  GET /api/children_categories
```

### *����� ����* - children_groups
```
  POST /api/cu_children_group { "code": "000000003", "name": "3\1", "children_category_code": "000000001", "institution_code": "14"}
  GET /api/children_group?code=000000003
  GET /api/children_groups
```

### *���� ������� ����* - children_categories_types
```
  POST /api/cu_children_categories_type { "code": "00000001", "name": "���������" }
  GET /api/children_categories_type?code=16
  GET /api/children_categories_types
```

### *������� ��������� ������* - reasons_absences
```
  POST /api/cu_reasons_absence { "code": "000000001", "mark": "�", "name": "�������" }
  GET /api/reasons_absence?code=000000001
  GET /api/reasons_absences
```

## ���������
### *���������� �������������* - supplier_orders
```
  POST /api/cu_supplier_order
  { "branch_code": "00000000006", "supplier_code": "00000000023", "number": "00000011", "date": 1495542284, "date_start": 1498867200, "date_end": 1519862400, "products": [ { "institution_code": "14", "product_code": "000000079", "contract_number": "BX-0000001", "date": 1495542284, "count": 12, "price": 10.05}, {"institution_code": "14", "product_code": "000000046  ", "contract_number": "BX-0000001", "date": 1495628684, "count": 15, "price": 17.12 } ] }
  GET api/supplier_order?supplier_order?branch_code=0003&number=00000011
  DELETE api/supplier_order { "branch_code": "00000000003", "number": "000000000002" }
```

### *����������� ���* - receipts
```
  POST /api/cu_receipt
  { "institution_code": "14", "supplier_order_number": "000000000002", "contract_number": "��-000000001", "number": "0000000000011", "invoice_number": "00000012", "date": "1485296673", "date_sa": "1485296673", "number_sa": "000000000001", "products": [ { "product_code": "000000079", "date": "1504224000", "count": 25, "count_invoice": 25, "causes_deviation_code": "" }, { "product_code": "000000046", "date": "1504224000", "count": 19, "count_invoice": 30, "causes_deviation_code": "000000002" } ] }
  GET /api/receipt?/receipt?institution_code=14&number=KL-000000005
  DELETE /api/receipt { "institution_code": "14", "number": "000000000002" }
```

### *���������� �������� ����������* - institution_orders
```
  POST /api/cu_institution_order
  { "institution_code": "14", "number": "000000000002", "date": "1485296673", "date_start": "1485296673", "date_end": "1485296673", "date_sa": "1485296673", "number_sa": "000000000001", "products": [ { "date": "1485296673", "product_code": "000000079  ", "count": 15, "description": "1 �������"}, { "date": "1485296673", "product_code": "000000048  ", "count": 15, "description": "1 �������,3 �������" } ] }
  GET api/institution_order?institution_code=14&number=000000000002
  DELETE api/institution_order { "institution_code": "14", "number": "000000000002" }
```

### *������������ ���������� �������� ����������* - io_corrections
```
  POST /api/cu_institution_order_correction
  { "institution_code": "14", "institution_order_number": "000000000002", "number": "000000000004", "date": "1485296673", "date_sa": "1485296673", "number_sa": "000000000001", "products": [ { "date": "1485296673", "product_code": "000000079", "diff": 7, "description": "1 �������" }, { "date": "1485296673", "product_code": "000000048  ", "diff": 5, "description": "1 �������,3 �������" } ] }
  GET /api/institution_order_correction?institution_code=14&institution_order_number=000000000002&number=000000000010
  DELETE /api/institution_order_correction { "institution_code": "14", "institution_order_number": "KL-000000024", "number": "KL-000000011" }

```

### *����-������* - menu_requirements
����
```
  POST /api/cu_menu_requirement_plan
  { "branch_code": "0003", "institution_code": "14", "number": "000000000002", "date": "1485296673", "splendingdate": "1485296673", "date_sap": "1485296673", "number_sap": "000000000001", "children_categories": [ { "children_category_code": "000000001", "count_all_plan": 55, "count_exemption_plan": 19 }, { "children_category_code": "000000002", "count_all_plan": 3, "count_exemption_plan": 7 } ], "products": [ { "children_category_code": "000000001", "product_code": "000000079  ", "count_plan": 15 }, { "children_category_code": "000000002", "product_code": "000000079  ", "count_plan": 21 } ] }
```
����
```
  POST /api/cu_menu_requirement_fact
  { "branch_code": "0003", "institution_code": "14", "number": "000000000002", "date": "1485296673", "splendingdate": "1485296673", "date_saf": "1485296673", "number_saf": "000000000001", "children_categories": [ { "children_category_code": "000000001", "count_all_fact": 55, "count_exemption_fact": 19 }, { "children_category_code": "000000002", "count_all_fact": 3, "count_exemption_fact": 7 } ], "products": [ { "children_category_code": "000000001", "product_code": "000000079  ", "count_fact": 15 }, { "children_category_code": "000000002", "product_code": "000000079  ", "count_fact": 21 } ] }
```
�������
```
  GET api/menu_requirement?institution_code=14&number=000000000028
  DELETE api/menu_requirement { "institution_code": "14", "number": "000000000002" }
```
### *������* - timesheets
```
  POST /api/cu_timesheet
  { "branch_code": "0003", "institution_code": "14", "number": "000000000002", "date": "1487548800",
     "date_vb": "1485907200", "date_ve": "1488240000", "date_eb": "1485907200", "date_ee": "1486684800", "date_sa": "1506902400", "number_sa": "000000000001", "dates": [ { "child_code": "000000001", "children_group_code": "000000001", "reasons_absence_code": "000000001", "date": "1485907200" }, { "child_code": "000000001", "children_group_code": "000000001", "reasons_absence_code": "000000001", "date": "1485993600" } ] }
  GET api/timesheet?institution_code=14&number=000000000001
  DELETE api/timesheet { "institution_code": "14", "number": "000000000002" }
```
