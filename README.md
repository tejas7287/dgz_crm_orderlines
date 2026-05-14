# CRM Order Lines

**Version:** 19.0.1  
**Category:** CRM  
**License:** LGPL-3  
**Author:** Digitz Technologies
**Website:** www.digitztech.com

## Description

With this module, you can generate sales order lines directly from CRM.
        Clicking the 'New Quotation' button in CRM opens the corresponding sale order,
        preloaded with default order lines that were initially saved in CRM.

## Features

- Odoo 19.0 compatible
- Addon module


## Dependencies

This module depends on the following Odoo modules:

- `crm`
- `sale_crm`
- `sale_management`
- `sale_stock`
- `sale_purchase`
- `zb_product_approve`

## Installation

1. Clone this repository into your Odoo addons directory:
   ```bash
   git clone https://github.com/tejas7287/dgz_crm_orderlines.git
   ```

2. Add the module path to your Odoo configuration file (`odoo.conf`):
   ```
   addons_path = /path/to/odoo/addons,/path/to/dgz_crm_orderlines
   ```

3. Restart the Odoo server:
   ```bash
   sudo systemctl restart odoo
   ```

4. Go to **Apps** → **Update Apps List** → Search for **"CRM Order Lines"** → Click **Install**

## Module Structure

```
dgz_crm_orderlines/
├── __init__.py
├── __manifest__.py
├── models/
├── security/
├── static/
├── views/
├── {models,views,security,static/
```

## Configuration

After installation, configure the module through Odoo's Settings menu or the module's specific configuration options.

## License

This project is licensed under the LGPL-3 License.

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request
