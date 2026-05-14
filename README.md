# CRM Order Lines

![Version](https://img.shields.io/badge/version-19.0.1-blue)
![Category](https://img.shields.io/badge/category-CRM-green)
![License](https://img.shields.io/badge/license-LGPL-3-orange)

| | |
|---|---|
| **Name** | CRM Order Lines |
| **Version** | 19.0.1 |
| **Category** | CRM |
| **Author** | Digitz Technologies |
| **License** | LGPL-3 |
| **Application** | No (Addon) |
| **Website** | www.digitztech.com |

## Description

With this module, you can generate sales order lines directly from CRM.
        Clicking the 'New Quotation' button in CRM opens the corresponding sale order,
        preloaded with default order lines that were initially saved in CRM.

## Functionality

### Models & Fields

#### `crm.lead.products` — CRM Lead Order Line

**File:** `models/crm.py`

**Inherits:** `crm.lead`

**Fields:**

| Field | Type |
|-------|------|
| `order_line_ids` | `One2many` |
| `crm_currency_id` | `Many2one` |
| `total` | `Monetary` |
| `lead_id` | `Many2one` |
| `product_id` | `Many2one` |
| `name` | `Text` |
| `product_uom_qty` | `Float` |
| `price_unit` | `Float` |
| `company_id` | `Many2one` |
| `currency_id` | `Many2one` |
| `price_subtotal` | `Monetary` |

**Key Methods:**

- `action_new_quotation()` — Action/workflow method
- `_compute_total()` — Computed field
- `_onchange_product_id()` — Onchange handler
- `_compute_subtotal()` — Computed field

#### Extends `sale.order, sale.order.line`

**File:** `models/sale.py`

**Inherits:** `sale.order`, `sale.order.line`

**Fields:**

| Field | Type |
|-------|------|
| `vendor_ids` | `Many2many` |
| `is_dropship` | `Boolean` |

**Key Methods:**

- `action_confirm()` — Action/workflow method
- `_get_dropship_picking_type()`
- `_onchange_sale_order_template_id()` — Onchange handler

### Views & UI

**List/Tree Views:** `crm.xml`

### Security

**Access Rights:** 1 model access rules defined

| Model |
|-------|
| `access_crm_lead_products` |

## Dependencies

| Module | Type |
|--------|------|
| `crm` | Odoo Core |
| `sale_crm` | Odoo Core |
| `sale_management` | Odoo Core |
| `sale_stock` | Odoo Core |
| `sale_purchase` | Odoo Core |
| `zb_product_approve` | Custom |

## File Structure

```
dgz_crm_orderlines/
├── LICENSE
├── README.md
├── __init__.py
├── __manifest__.py
├── models/
│   ├── __init__.py
│   ├── crm.py
│   └── sale.py
├── security/
│   └── ir.model.access.csv
├── static/
│   └── description/
│       ├── BRANDIND-ICON-1.png
│       ├── CRM-.png
│       ├── MARKETING-CAMPIGNS-.png
│       ├── SCALABILITY.png
│       ├── SUPPORT-TEAM.png
│       ├── WEB-DEVELOPMENT-3.png
│       ├── assets/
│       ├── creating_project.png
│       ├── first.png
│       ├── fourth.png
│       ├── icon.png
│       ├── index.html
│       ├── second.png
│       ├── third.png
│       └── thumbnail.gif
├── views/
│   ├── crm.xml
│   └── sale.xml
└── {models,views,security,static/
    └── description}/
```

## Installation

This module is part of the **[odoo-crm-sales-suite](https://github.com/tejas7287/odoo-crm-sales-suite)** suite.

1. Place this module in your Odoo addons directory
2. Update the apps list: **Settings** → **Apps** → **Update Apps List**
3. Search for **"CRM Order Lines"** and click **Install**

## License

LGPL-3
