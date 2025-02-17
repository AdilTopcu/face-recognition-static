# **Face Feature Comparison with Weighted Functions**

This MATLAB program compares various facial features such as eye, nose, lip, and face proportions. It uses a set of weighted functions and predefined values for each individual's facial features. The script calculates weighted differences between input features and predefined (registered) values to assess identity matching.

## **Functions:**

- **A(x), B(x), C(x), D(x), E(x), F(x), G(x), H(x)**: These are functions that perform transformations on the input values based on predetermined thresholds.

## **Predefined User Data:**
The following predefined facial features are used for comparisons:
- **Adilin's Face Features**: Göz Orani, Burun Orani, Yüz Orani, Dudak Orani, Yüzün Rengi.
- **Emin's Face Features**
- **Ege's Face Features**
- **Izzet's Face Features**
- **Melis's Face Features**

These data points are stored as matrices and used for comparison during the identity verification process.

## **How It Works:**

1. **Input Data**:
   - The program assumes that facial features are represented by certain proportions for different individuals (e.g., `AdilinGozOrani` for Adilin's eye proportion).

2. **Transformation of Data**:
   - The program applies different mathematical functions (A-H) to the input facial feature data, based on their respective thresholds.

3. **Weighted Calculation**:
   - The program compares the input features with predefined data and calculates weighted differences based on the closeness of the data points using custom weights.

4. **Matrix Operations**:
   - The script creates matrices to calculate the weighted differences between the features for each individual. These matrices are later used to determine how closely the input features match the registered features.

5. **Distance and Similarity**:
   - It calculates the difference between the input and registered matrices and generates a weight for each comparison.
   - If the average weighted difference (based on the weight matrix) is below a threshold (0.06), the identity is considered a match.

## **Outputs:**

- **Weighted Matrices**: Calculated matrices for each individual's facial feature comparison.
- **Identity Validation**: For each individual (Adilin, Emin, Ege, Izzet, Melis), the program checks if their input features match the registered features based on a similarity threshold. 

## **Example Workflow:**

### **Step 1: Predefined Data (Features)**

The program has predefined matrices for each person (e.g., Adilin, Emin, Ege, Izzet, Melis). These matrices include values for features like `AdilinGozOrani`, `AdilinBurunOrani`, etc.

### **Step 2: Calculating Weighted Differences**

- For each facial feature matrix, the program applies functions (A-H) based on predefined thresholds to transform the feature values.
  
### **Step 3: Weighting Based on Feature Differences**

- The program calculates how close the input values are to the registered data by using a weighted distance matrix.

### **Step 4: Identity Check**

- The program calculates the weighted average of the differences for each individual. If the difference is less than or equal to 0.06, it outputs:
    ```
    "Identity verification successful for [Name]"
    ```
    Otherwise:
    ```
    "Please try again"
    ```

### **Sample Output:**
