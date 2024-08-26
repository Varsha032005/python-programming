import time
import random

def measure_concentration(pollutant):
    return random.uniform(0, 100)

def calculate_sub_api(concentration):
    return concentration * 0.5

def classify_api(api_value):
    if api_value <= 50:
        return "Good"
    elif api_value <= 100:
        return "Moderate"
    elif api_value <= 150:
        return "Unhealthy for Sensitive Groups"
    elif api_value <= 200:
        return "Unhealthy"
    elif api_value <= 300:
        return "Very Unhealthy"
    else:
        return "Hazardous"

def main():
    while True:
        co_concentration = measure_concentration('CO')
        o3_concentration = measure_concentration('O3')
        pm10_concentration = measure_concentration('PM10')
        pm25_concentration = measure_concentration('PM2.5')
        
        sub_api_co = calculate_sub_api(co_concentration)
        sub_api_o3 = calculate_sub_api(o3_concentration)
        sub_api_pm10 = calculate_sub_api(pm10_concentration)
        sub_api_pm25 = calculate_sub_api(pm25_concentration)
        
        api_value = max(sub_api_co, sub_api_o3, sub_api_pm10, sub_api_pm25)
        
        api_classification = classify_api(api_value)
        
        print(f"API Value: {api_value:.2f} - {api_classification}")
        print(f"Storing API value {api_value:.2f} to SD card...")
        
        end_process = input("End? (Y/N): ").strip().lower()
        if end_process == 'y':
            break
        time.sleep(5)
if __name__ == "__main__":
    main()
