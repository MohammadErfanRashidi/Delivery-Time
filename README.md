# Food Delivery Time Prediction

This project aims to predict the delivery time for food orders using machine learning. It utilizes historical data on delivery details, including delivery person information, order details, and location data. 

## Dataset

The project uses the 'deliverytime.txt' dataset, which contains the following columns:

- Delivery_person_ID: Unique identifier for the delivery person
- Delivery_person_Age: Age of the delivery person
- Delivery_person_Ratings: Average ratings of the delivery person
- Restaurant_latitude: Latitude coordinates of the restaurant
- Restaurant_longitude: Longitude coordinates of the restaurant
- Delivery_location_latitude: Latitude coordinates of the delivery location
- Delivery_location_longitude: Longitude coordinates of the delivery location
- Order_Date: Date of the order
- Time_Orderd: Time the order was placed
- Time_Order_picked: Time the order was picked up from the restaurant
- Weather conditions: Weather conditions during the delivery
- Road_traffic_density: Traffic density on the road
- Vehicle_condition: Condition of the delivery vehicle
- Type_of_order: Type of order (e.g., food, groceries)
- Type_of_vehicle: Type of vehicle used for delivery
- multiple_deliveries: Number of simultaneous deliveries
- Festival: Whether a festival was ongoing during the delivery
- City: City where the delivery took place
- Time_taken(min): Total time taken for the delivery (target variable)

## Methodology

1. **Data Loading and Preprocessing:** The dataset is loaded using Pandas, and missing values are handled.
2. **Distance Calculation:** The geodesic distance between the restaurant and the delivery location is calculated using the `geopy` library.
3. **Exploratory Data Analysis:** Scatter plots are generated to visualize the relationships between delivery time and features such as distance, delivery person ratings, and age. Box plots are used to analyze the relationship between delivery time and the type of vehicle and order.
4. **Feature Selection:** Relevant features (delivery person age, ratings, and distance) are selected for model training.
5. **Model Training:** An LSTM neural network is implemented using Keras to predict delivery time. The model is trained on a portion of the data.
6. **Model Evaluation:** The model's performance is evaluated on a test dataset using appropriate metrics.
7. **Prediction:** The trained model can predict the delivery time for new orders based on input features.

## Requirements

- Python 3.x
- Pandas
- NumPy
- Plotly
- Geopy
- Scikit-learn
- Keras
- TensorFlow

## Usage

1. Install the required libraries: `pip install pandas numpy plotly geopy scikit-learn keras tensorflow`
2. Run the code in a Google Colab environment or a Jupyter Notebook.
3. Provide input values for delivery person age, ratings, and distance to obtain the predicted delivery time.


## Contributing

Contributions to this project are welcome! Please feel free to open issues or submit pull requests for bug fixes, enhancements, or new features.


## License

This project is licensed under the MIT License.
