## Flask GraphQL Demo

## Installation

1. Activate a virtual environment
1. Install dependencies with pip
1. Install sample data in `./install_database.py`
1. Run server `./server.py`
1. Test service at http://127.0.0.1:5000/
    ```
    {
      allEmployees {
        edges {
          node {
            name
            hiredOn

            department {
              name
            }
          }
        }
      }
    }
    ```

    ```
    {
      department(id:"RGVwYXJ0bWVudDox"){
        id
        name
        employees {
          edges{
            node {
              name
              hiredOn
            }
          }
        }
      }
    }
    ```

## Code Quality

- Pylint `pylint flask-graphql`
- Nose Unit Tests `nosetests tests/`