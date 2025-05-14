# Agricultural Yield Prediction and Risk Assessment

### Note:
This is my final project for a machine learning course (BU425) that I took during my undergrad at the Wilfrid Laurier University. Due to course policies, I am not permitted to share the source code publicly. In case you are interested in learning more about the project or accessing the source code, please reach out to me at yhbarve@uwaterloo.ca.

---

## Project Overview
 This project develops a machine learning system to predict agricultural crop yields and assess associated risks. By leveraging historical data on climate, pesticide usage, and crop performance, the model provides farmers and agricultural stakeholders with actionable insights to optimize yields and mitigate environmental risks.

## Key Features
- **Yield Prediction**: LSTM neural network model to forecast crop yields based on historical patterns
- **Risk Assessment**: Comprehensive risk scoring system considering rainfall, temperature, pesticide usage, and yield deviation
- **Feature Engineering**: Advanced temporal feature creation including rolling averages, lag indicators, and change metrics
- **Data Visualization**: Graphical representations of yield distributions and risk assessments

## Technologies Used
- **Python**: Primary programming language
- **TensorFlow/Keras**: Deep learning framework for LSTM model implementation
- **Scikit-learn**: Machine learning library for Random Forest model and data preprocessing
- **Pandas/NumPy**: Data manipulation and numerical operations
- **Matplotlib/Seaborn**: Data visualization

## Methodology

### Data Preprocessing
1. Log transformation of yield data to normalize distribution
2. Feature engineering:
   - Rolling averages for rainfall and temperature
   - Year-over-year changes in climate metrics
   - Lagged indicators (previous year values)
3. Normalization using MinMaxScaler

### Model Development
1. **Random Forest Regressor**:
   - Feature importance analysis
   - Hyperparameter optimization via GridSearchCV
   - Identification of key yield predictors
   
2. **LSTM Neural Network**:
   - Sequential data preparation with 5-year lookback window
   - Two-layer architecture with dropout for regularization
   - Adam optimizer with MSE loss function

### Risk Assessment Framework
The risk scoring algorithm evaluates:
- Drought and flood risks based on rainfall patterns
- Temperature anomalies and extremes
- High pesticide usage concerns
- Yield deviations from historical averages

Risk scores are calculated using dynamic weighting that prioritizes severe risk factors and accounts for interaction effects between multiple risk sources.

## Results
- Achieved low Mean Squared Error (MSE) of 0.0094 on test data
- Identified pesticide usage and temperature patterns as primary yield determinants
- Created risk distribution visualization showing majority of scenarios in low-to-medium risk categories

## Future Improvements
- Integration of satellite imagery data
- Incorporation of soil quality metrics
- Real-time monitoring capabilities
- Expanded crop variety coverage
- Climate change scenario modeling

## Usage
The model can be utilized by:
- Agricultural cooperatives for yield forecasting
- Insurance companies for risk assessment
- Government agencies for food security planning
- Individual farmers for crop management decisions

## Contributors
- Yash Barve, Nicholas Rebello, Amy Freij Camacho, Wang Qianyi

## License
Please get in touch with me at yhbarve@uwaterloo.ca to learn more.
