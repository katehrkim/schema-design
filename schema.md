#Visualize your schema

Open this file in your text editor and visualize your schema. At the top is your table name. Listed below are all the columns in that table. 

User
-------------------
id
first_name
last_name

Address
-------------------
id
user_id
street 
street2 
city
state
zip_code
country

In the example above, each Address can belong to a User. This is achieved by adding a column called `user_id`, which can match only ONE of the values in the `id` column of the User table. Remember, `id`s are unique; no table can have two `id` values that are the same.

Using the above format, jot down the database for your apps below!

## GrubHub Online Ordering

users:
id (*)
first_name (need)
last_name (opt)

orders:
id (*)
date (need)
user_id (need)
menu_id (need)

menus:
id (*)
menu_name (need)
restaurant_id (need)

restaurants:
id (*)
name (need)

## Blue Apron

users:
id (*)
first_name (need)
last_name (opt)
service_plan_id (opt)
promo_id (opt)
delivery_id (need)

service_plans:
id (*)
plan_name (need)
price_per_serving (need)
recipes_per_week (need)
serving_size (need)

recipes:
id (*)
recipe_name (need)
service_plan_id (opt)
prep_time (opt)

promotions:
id (*)
promo_name (need)
detail (opt)

deliveries:
id (*)
price_per_shipping (need)

## Instagram

users:
id (*)
first_name (need)
last_name (opt)
insta_handle (need)
num_followers (opt)
num_following (opt)
num_posts (opt)

posts:
id (*)
user_id (need)
date (need)
num_likes (opt)
num_comments (opt)

likes:
id (*)
user_id (need)
post_id (need)

comments:
id (*)
user_id (need)
message (need)
post_id (need)

follow:
id (*)
follower_user_id (need)
followed_user_id (need)
