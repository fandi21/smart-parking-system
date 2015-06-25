# Team Skills 6: Building the Right System #

# 1.0 Test Case 1: Test the reservation system. #
## 1.1 Use Case scenarios ##

<img src='http://i39.tinypic.com/28b5rx5.jpg' />

## 1.2 Basic Flow of Use Case ##

| **B1** | **Enter to the website.** |
|:-------|:--------------------------|
| **B2** | **Choose the date and the time and the period.** |
| **B3** | **Enter the payment method.** |
| **B4** | **Receive the password for the spot.** |

## 1.3 Alternative Flow ##

| **A1** | **Re-choose the date or the time or the period, because no available spot.** |
|:-------|:-----------------------------------------------------------------------------|
| **A2** | **The payment method not work, re-enter correct method.**                    |

## 1.4 Identify Use Case scenarios ##

| **Scenario Number** | **Original Flow** | **Alternative Flow1** | **Alternative Flow2** | **Alternative Flow3** |
|:--------------------|:------------------|:----------------------|:----------------------|:----------------------|
| **1**               | **Basic Flow**    | **-**                 | **-**                 | **-**                 |
| **2**               | **Basic Flow**    | **Alt. Flow 1**       | **-**                 | **-**                 |
| **3**               | **Basic Flow**    | **Alt. Flow 2**       | **-**                 | **-**                 |
| **4**               | **Basic Flow**    | **Alt. Flow 1**       | **Alt. Flow 2**       | **-**                 |

## 1.5 Variables Identified ##

| **Variables ID** | **Variables** | **Option to be Tested** |
|:-----------------|:--------------|:------------------------|
| **1**            | **The date.** | **Available date.**     |
| **2**            | **The time.** | **Available time.**     |
| **3**            | **The time for the reservation.** | **Available any period.** |
| **4**            | **Type of payment method.** | **Available Visa, Master, GU gold.** |

## 1.6 Test Case ##

| **Test Case ID** | **Scenario** | **Description** | **Condition 1** | **Condition 2** | **Condition 3** | **Expected result** |
|:-----------------|:-------------|:----------------|:----------------|:----------------|:----------------|:--------------------|
| **RS 1**         | **1**        | **Basic Flow. Enter a date and a time and the period for the reservation. The date and time shouldn’t before now.** | **Enter date. (mm/dd/yyyy)** | **Enter time. 24 h format like (hh:mm)** | **Enter the period. From (hh:mm) to (hh:mm)** | **Go to next step** |
| **RS 2**         | **1**        | **Alt. Flow1. Enter a date or time or period not available for reservation.** | **Enter date. (dd/mm/yyyy)** | **Enter time. hh:mm PM** | **Enter the period. From (hh:mm) to (hh:mm)** | **The massage show that is please enter another time.** |
| **RS 3**         | **1**        | **Alt. Flow1. Enter a date and time not correct.** | **Enter date. (mm/dd/yyyy)** | **Enter time. hh:mm PM** | **-**           | **The massage show that is please enter correct format.** |
| **RS 4**         | **2**        | **Basic Flow. Enter you payment method** | **Enter type of payment method.** | **Enter holder name and card number** | **Enter exp date and CSC.** | **You will receive the password for the spot.** |
| **RS 5**         | **2**        | **Alt. Flow2. Enter wrong payment method** | **Enter type of payment method.** | **Enter holder name and card number** | **Enter exp date and CSC.** | **The massage show that is please enter correct card # or CSC.** |

# 2.0 Test Case 2: Test the Screen in each Floor. #
## 2.1 Use Case scenarios ##

<img src='http://i42.tinypic.com/egobia.jpg' />

## 2.2 Basic Flow of Use Case ##

| **B1** | **The operator enters the number for the empty spot.** |
|:-------|:-------------------------------------------------------|
| **B2** | **The system calculateshow many empty spot in each floor.** |
| **B3** | **The screen show how many empty spot in each floor.** |

## 2.3 Alternative Flow ##

| **A1** | **A car enters to a floor.** |
|:-------|:-----------------------------|
| **A2** | **A car leaves a floor.**    |

## 2.4 Identify Use Case scenarios ##

| **Scenario Number** | **Original Flow** | **Alternative Flow1** | **Alternative Flow2** | **Alternative Flow3** |
|:--------------------|:------------------|:----------------------|:----------------------|:----------------------|
| **1**               | **Basic Flow**    | **-**                 | **-**                 | **-**                 |
| **2**               | **Basic Flow**    | **Alt. Flow 1**       | **-**                 | **-**                 |
| **3**               | **Basic Flow**    | **Alt. Flow 2**       | **-**                 | **-**                 |
| **4**               | **Basic Flow**    | **Alt. Flow 1**       | **Alt. Flow 2**       | **-**                 |
| **5**               | **Basic Flow**    | **Alt. Flow 2**       | **Alt. Flow 1**       | **-**                 |

## 2.5 Variables Identified ##

| **Variables ID** | **Variables** | **Option to be Tested** |
|:-----------------|:--------------|:------------------------|
| **1**            | **Decrease the empty spotin the screen.** | **Cross a car the sensor line and weight sensor.** |
| **2**            | **Increase the empty spot in the screen.** | **Cross a car the sensor line and weight sensor.** |

## 2.6 Test Case ##

| **Test Case ID** | **Scenario** | **Description** | **Condition 1** | **Condition 2** | **Condition 3** | **Expected result** |
|:-----------------|:-------------|:----------------|:----------------|:----------------|:----------------|:--------------------|
| **RS 1**         | **1**        | **Basic Flow. A car enter a floor and cross the sensor line and a tire press the weight sensor** | **A car cross the sensor line.** | **A tire for a car press on the weight sensor.** | **-**           | **The number for the empty spot will decrease by one.** |
| **RS 2**         | **1**        | **Alt. Flow1. If there something cross the sensor line, but there isn’t the weight sensor active it.** | **A car cross the sensor line.** | **There isn’t enough to press on the weight sensor.** | **-**           | **The number for the empty spot stills the same.** |
| **RS 3**         | **2**        | **Basic Flow. A car leave a floor and cross the sensor line and a tire press the weight sensor** | **A car cross the sensor line.** | **A tire for a car press on the weight sensor.** | **-**           | **The number for the empty spot will increase by one.** |
| **RS 4**         | **2**        | **Alt. Flow2. If there something cross the sensor line, but there isn’t the weight sensor active it.** | **A car cross the sensor line.** | **There isn’t enoughto press on the weight sensor.** | **-**           | **The number for the empty spot stills the same.** |