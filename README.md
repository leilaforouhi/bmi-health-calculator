# bmi-health-calculato
A Python script to calculate Body Mass Index (BMI) and provide health status categories.
def calculate_bmi(weight_kg, height_m):
    bmi = weight_kg / (height_m ** 2)
    return round(bmi, 2)

def get_category(bmi):
    if bmi < 18.5: return "Underweight"
    elif 18.5 <= bmi < 25: return "Normal weight"
    elif 25 <= bmi < 30: return "Overweight"
    else: return "Obese"

if __name__ == "__main__":
    w, h = 75, 1.80
    result = calculate_bmi(w, h)
    print(f"BMI: {result} - Category: {get_category(result)}")
