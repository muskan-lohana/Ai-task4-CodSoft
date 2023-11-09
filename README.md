# Ai-task4-CodSoft
# Product Recommendation System

This is a simple product recommendation system created using the LightFM library. It provides recommendations for products to users based on their interactions and product features. The system combines collaborative filtering and content-based filtering to generate personalized recommendations.

## How It Works

1. **Data Setup**: The system is set up with two key datasets:

   - `products_data`: Information about the products, including their IDs, names, and features.
   - `user_data`: Information about user interactions, including user IDs and product interactions.

2. **Data Preprocessing**: The system preprocesses the data and prepares it for modeling.

3. **Model Creation**: A hybrid recommendation model is created using LightFM. This model combines both collaborative and content-based filtering.

4. **Recommendation**: Users can request recommendations for specific users. The model predicts the top products that the user is likely to be interested in and provides the product names.

## Usage

1. **Data Configuration**: Replace the example data in `products_data` and `user_data` with your own product and user data.

2. **Model Training**: The model is trained using the `LightFM` library. You can adjust the parameters and training epochs according to your needs.

3. **Generating Recommendations**: Use the `recommend_products` function to generate recommendations for a specific user. Replace `user_id` with the user ID for whom you want recommendations.

4. **View Recommendations**: The recommended products for the user are displayed in the console.

## Example

```python
user_id = 1  # Replace with the user ID for whom you want to make recommendations
recommended_products = recommend_products(user_id, model, products_data, dataset)
print(f"Recommended products for user {user_id}:")
for i, product_name in enumerate(recommended_products):
    print(f"{i + 1}. {product_name}")

## Dependencies
LightFM
NumPy
