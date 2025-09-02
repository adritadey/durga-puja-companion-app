# 🕉️ Durga Puja Companion App – UX Design + Python Prototype

## 📌 Overview
This project blends UX design and Python logic to simulate a mobile app that enhances the Durga Puja experience for citizens in Kolkata. Originally designed in Figma, the app provides personalized pandal recommendations, crowd alerts, accessibility guidance, and notification preferences. The Python prototype simulates backend logic and user flows to complement the visual design.

---

## 🎯 Objectives
- Design a user-friendly interface for Durga Puja navigation and updates
- Simulate backend logic using Python for personalized experiences
- Blend UX strategy with functional prototyping to showcase end-to-end thinking

---

## 🛠️ Tools Used
- **Figma** – UX design and wireframes
- **Python** – Backend simulation and user flow logic
- **Streamlit** (optional future extension) – GUI interface for live interaction

---

## 👤 Simulated User Profiles
```python
users = [
    {"name": "Ananya", "location": "Salt Lake", "prefers_notifications": True, "accessibility_needs": False},
    {"name": "Rohit", "location": "Behala", "prefers_notifications": False, "accessibility_needs": True},
    {"name": "Meera", "location": "Park Circus", "prefers_notifications": True, "accessibility_needs": False}
]
🏕️ Pandal Data
pandals = {
    "Salt Lake": {"theme": "Eco-Friendly", "crowd_level": "Moderate", "accessible": True},
    "Behala": {"theme": "Mythical Legends", "crowd_level": "High", "accessible": False},
    "Park Circus": {"theme": "Digital Bengal", "crowd_level": "Low", "accessible": True}
}
🔄 UX Logic Simulation
def generate_user_experience(users, pandals):
    for user in users:
        zone = user["location"]
        pandal = pandals.get(zone, {})
        print(f"\nHi {user['name']}! Here's your Durga Puja plan:")
        print(f"• Theme in {zone}: {pandal.get('theme', 'Unknown')}")
        print(f"• Crowd Level: {pandal.get('crowd_level', 'Unknown')}")
        
        if user["prefers_notifications"]:
            print("• You’ll receive live updates and alerts.")
        
        if user["accessibility_needs"] and not pandal.get("accessible", False):
            print("⚠️ This pandal may not be accessible. Consider visiting Park Circus instead.")
        elif user["accessibility_needs"]:
            print("• This pandal is accessible and senior-friendly.")

🧩 Additional Features
🗣️ Interactive User Input
name = input("Enter your name: ")
location = input("Enter your neighborhood: ")

⚠️ Crowd Level Alerts
if pandal["crowd_level"] == "High":
    print("⚠️ Expect heavy crowds. Visit early or choose a less crowded pandal.")

📄 Export Personalized Plan to File
with open(f"{user['name']}_puja_plan.txt", "w") as file:
    file.write(f"Your Durga Puja plan for {zone}:\nTheme: {pandal['theme']}\nCrowd Level: {pandal['crowd_level']}")

🖥️ GUI Version (Streamlit or Tkinter)
Create a visual interface with dropdowns, buttons, and map views

Display pandal recommendations interactively

Filter by accessibility and crowd level

🎨 UX Design Integration
Home screen: Personalized greeting and pandal suggestions

Map view: Color-coded crowd levels

Accessibility toggle: Filters pandals based on mobility access

Notification center: Live updates and alerts

📁 Repository Structure
Code
/
├── durga_puja_prototype.py             # Python simulation file
├── README.md                           # Project overview
├── /screenshots                        # Figma design screenshots
│   ├── home_screen.png
│   ├── map_view.png
│   └── alert_center.png
🧠 Key Insights
UX design must adapt to real-time data like crowd density and accessibility

Python simulation helps validate user flows before full development

Combining design and logic creates a holistic user experience

Export and input features make the app more personalized and scalable
