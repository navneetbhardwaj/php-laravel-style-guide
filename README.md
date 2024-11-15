# PHP Naming Conventions for Laravel Projects 🎉

This guide describes naming conventions widely adopted within the Laravel community. These guidelines help standardize code across different projects, ensuring better readability, maintainability, and collaboration.

## Table of Contents

- [Controller Naming](#controller-naming)
- [Route Naming](#route-naming)
  - [Route URL](#route-url)
  - [Route Name](#route-name)
- [Database Naming](#database-naming)
  - [Migration](#migration)
  - [Table Names](#table-names)
  - [Pivot Tables](#pivot-tables)
  - [Table Columns](#table-columns)
  - [Foreign Key Naming](#foreign-key-naming)
  - [Primary Key Naming](#primary-key-naming)
- [Model Naming](#model-naming)
  - [Single Relation Methods](#single-relation-methods)
  - [Other Relation Methods](#other-relation-methods)
- [Function Naming](#function-naming)
- [Resource Controller Methods](#resource-controller-methods)
- [Variables](#variables)
- [Collections and Objects](#collections-and-objects)
  - [Collections](#collections)
  - [Objects](#objects)
- [Configuration Keys](#configuration-keys)
- [Traits](#traits)
- [Interfaces](#interfaces)

---

### Controller Naming
- **Singular** form
- **PascalCase** format

| Preferred              | Avoid                             |
|------------------------|-----------------------------------|
| `CustomerController.php` | `CustomersController.php`       |

### Route Naming

#### Route URL
- Use **Plural** form for URLs
- Use **kebab-case** for multi-word paths

| Preferred                        | Avoid                                  |
|----------------------------------|----------------------------------------|
| `/customers/25`<br> `/customers/password-reset` | `/customer/25`<br> `/customers/password_reset`<br> `/customers/passwordReset` |

#### Route Name
- **snake_case** with dot notation
- Should be descriptive and follow URL structure if possible

| Preferred                        | Avoid                                  |
|----------------------------------|----------------------------------------|
| `->('customers.view')`<br> `->('customers.password_reset')` | `->('customers-view')`<br> `->('customers_view')`<br> `->('customers.password-reset')`<br> `->('customer-password-reset')` |

### Database Naming

#### Migration
- **snake_case** format
- Descriptive, often reflecting the change

| Preferred                        | Avoid                                  |
|----------------------------------|----------------------------------------|
| `2021_03_19_033513_create_customers_table.php`<br> `2021_03_19_033513_add_image_id_to_customers_table.php` | `2021_03_19_033513_customers.php`<br> `2021_03_19_033513_add_image_id_customers.php` |

#### Table Names
- **Plural**
- **snake_case**

| Preferred              | Avoid                             |
|------------------------|-----------------------------------|
| `customers`, `cart_items` | `customer`, `cartItems`, `CartItems`, `Cart_item` |

#### Pivot Tables
- **Singular** form
- Alphabetical order with **snake_case**

| Preferred              | Avoid                             |
|------------------------|-----------------------------------|
| `course_student`       | `student_courses`, `course_students` |

#### Table Columns
- **snake_case**
- Avoid prefixing column names with table names

| Preferred              | Avoid                             |
|------------------------|-----------------------------------|
| `first_name`           | `user_first_name`, `FirstName`   |

#### Foreign Key Naming
- Singular form of the table name + `_id`
- **snake_case**

| Preferred              | Avoid                             |
|------------------------|-----------------------------------|
| `course_id`            | `courseId`, `courses_id`, `id_course` |

#### Primary Key Naming
- Use `id` for primary keys

| Preferred              | Avoid                             |
|------------------------|-----------------------------------|
| `id`                   | `custom_name_id`                 |

### Model Naming
- **Singular**
- **PascalCase**

| Preferred              | Avoid                             |
|------------------------|-----------------------------------|
| `Customer`             | `Customers`, `customer`          |

#### Single Relation Methods (Has One, Belongs To)
- **Singular** form
- **camelCase**

| Preferred              | Avoid                             |
|------------------------|-----------------------------------|
| `studentCourse`        | `StudentCourse`, `student_course` |

#### Other Relation Methods (Has Many, etc.)
- **Plural** form
- **camelCase**

| Preferred              | Avoid                             |
|------------------------|-----------------------------------|
| `cartItems`            | `CartItem`, `cart_item`, `cartItem` |

### Function Naming
- Use **snake_case**

| Preferred              | Avoid                             |
|------------------------|-----------------------------------|
| `show_route`           | `showRoute`, `ShowRoute`         |

### Resource Controller Methods
- Use **camelCase**
- Should generally be one-word actions

| Preferred              | Avoid                             |
|------------------------|-----------------------------------|
| `store`, `show`, `destroy`, `index` | `saveCustomer`, `viewCustomer`, `allCustomersPage` |

### Variables
- **camelCase**
- Use readable names to improve code clarity

| Preferred              | Avoid                             |
|------------------------|-----------------------------------|
| `$customerMessages`    | `$CustomerMessages`, `$customer_messages`, `$c_messages`, `$c_m` |

### Collections and Objects

#### Collections
- **Plural** form
- **camelCase**

| Preferred              | Avoid                             |
|------------------------|-----------------------------------|
| `$verifiedCustomers`   | `$verified`, `$data`, `$resp`, `$v_c` |

#### Objects
- **Singular** form
- **camelCase**

| Preferred              | Avoid                             |
|------------------------|-----------------------------------|
| `$verifiedCustomer`    | `$verified`, `$data`, `$resp`, `$v_c` |

### Configuration Keys
- **snake_case**
- Use descriptive, short names for clarity

| Preferred              | Avoid                             |
|------------------------|-----------------------------------|
| `comments_enabled`     | `CommentsEnabled`, `comments`, `c_enabled`, `$ce` |

### Traits
- Generally an **adjective**
- **PascalCase**

| Preferred              | Avoid                             |
|------------------------|-----------------------------------|
| `Utility`              | `UtilityTrait`, `Utilities`      |

### Interfaces
- Can be **adjective** or **noun**
- **PascalCase**

| Preferred              | Avoid                             |
|------------------------|-----------------------------------|
| `Authenticable`        | `AuthenticationInterface`, `Authenticate` |

---

By adhering to these naming conventions, your Laravel projects will be easier to read and maintain. Following consistent naming makes it simpler to understand code logic and enhances teamwork. Happy coding!
