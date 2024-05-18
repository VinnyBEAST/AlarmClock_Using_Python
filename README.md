### Logic Board by Vincent Nyanditu Nyang'aya, Software Engineer

1. **Objective:**
   - Create a Python program to set an alarm that plays a sound at a specified time.

2. **Gather Input:**
   - Prompt the user to enter the alarm time in the format `HH:MM:SS AM/PM`.

3. **Parse Input:**
   - Extract the hour, minute, second, and period (AM/PM) from the input string.

4. **Prepare for Loop:**
   - Inform the user that the alarm is being set up.

5. **Infinite Loop to Check Time:**
   - Continuously check the current time until it matches the specified alarm time.

6. **Fetch Current Time:**
   - Use `datetime.now()` to get the current date and time.
   - Format the current time to match the format used for comparison.

7. **Compare Current Time with Alarm Time:**
   - Check if the current period (AM/PM) matches the alarm period.
   - If the period matches, check if the current hour matches the alarm hour.
   - If the hour matches, check if the current minute matches the alarm minute.
   - If the minute matches, check if the current second matches the alarm second.

8. **Trigger Alarm:**
   - If all conditions are met, print "Wake Up!" and play the alarm sound using `playsound('audio.mp3')`.
   - Break the loop after the alarm triggers.

9. **Repeat Checks:**
   - If the conditions are not met, continue the loop and check the time again after a short delay.

### Steps Breakdown

1. **Prompt User for Input:**
   - `alarm_time = input("Enter the time of alarm to be set: HH:MM:SS AM/PM\n")`

2. **Extract Components from Input:**
   - `alarm_hour = alarm_time[0:2]`
   - `alarm_minute = alarm_time[3:5]`
   - `alarm_seconds = alarm_time[6:8]`
   - `alarm_period = alarm_time[9:11].upper()`

3. **Print Setup Message:**
   - `print("Setting up alarm..")`

4. **Start Infinite Loop:**
   - `while True:`

5. **Get Current Time:**
   - `now = datetime.now()`
   - `current_hour = now.strftime("%I")`
   - `current_minute = now.strftime("%M")`
   - `current_seconds = now.strftime("%S")`
   - `current_period = now.strftime("%p")`

6. **Check Time Conditions:**
   - `if (alarm_period == current_period):`
     - `if (alarm_hour == current_hour):`
       - `if (alarm_minute == current_minute):`
         - `if (alarm_seconds == current_seconds):`
           - `print("Wake Up!")`
           - `playsound('audio.mp3')`
           - `break`

### Additional Considerations

- **Error Handling:**
  - Validate the user input to ensure it is in the correct format.
  - Handle potential errors when playing the sound file.

- **Efficiency:**
  - Add a small delay in the loop to reduce CPU usage, e.g., `time.sleep(1)`.

- **Cross-Platform Compatibility:**
  - Ensure `playsound` is compatible with the operating system or use an alternative method for playing sound if needed.

### Final Thoughts

- The program is designed to be simple and functional, focusing on setting and triggering an alarm based on user input.
- Ensuring the robustness and user-friendliness of the program through validation and error handling is important for a better user experience.






