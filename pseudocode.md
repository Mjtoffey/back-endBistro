MoSCoW

    Must haves
      -CRUD Read operations
      -Table relationships (one to many, many to one)
      -url routes/paths to direct to appropriate view
      -be used to update react restaurant API call
    Should haves
      -full readability of menu items
      -many to many table relationship for better user manuverability
    Could haves
      -users to assign permissions to
      -generate a CSV
    Wont haves
      -DnD references or RPG elements


File Structure

      
      Table menu_items {
        id integer [primary key]
        name varchar
        description varchar
        cuisine varchar
        meal_type varchar
        spicy_level integer
        price integer 
      }
      
      Table cuisine {
        id integer [primary key]
        cuisine_type varchar
      }
      
      Table meal_type {
        id integer [primary key]
        meal_type_category varchar
      }
      
      Table spicy_level {
        id integer [primary key]
        spicy_rating integer
      }
      
      
      
      Ref: menu_items.cuisine > cuisine.id // many-to-one
      
      Ref: menu_items.meal_type > meal_type.id
      
      Ref: menu_items.spicy_level > spicy_level.id



Paths

    -/menu_items (all)
    -/breakfast
    -/lunch
    -/dinner
    -/appetizers
    -/cuisine


      
