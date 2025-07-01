# Food-apps-offer-analysis-reverse-engineering-

# 🧠 Reverse Engineering First-Time User Offers on Food Delivery Apps (Swiggy & Zomato)

## 📌 Overview

This self-initiated research explores how food delivery platforms like **Swiggy** and **Zomato** implement and restrict *first-time user* promotional offers. By experimenting with multiple accounts, devices, SIM cards, and login methods, I was able to uncover how these systems determine "new users" — and how their logic evolved to close existing loopholes.

The findings reflect real-world system behavior, user fingerprinting strategies, and ethical questions surrounding platform exploitation.

---

## 🔍 Platforms Analyzed
- **Swiggy**
- **Zomato**

---

## 🧪 Methodology

### 🟠 Swiggy Testing

- Created multiple new accounts using different mobile numbers and the same device.
- Repeated process: deleted old accounts, created new ones using the same number.
- Observed that Swiggy initially allowed coupon reuse when the account was recreated.
- Used different devices and networks to test further — found that coupon restrictions were *not just tied to phone number*, but also **device ID**.
- Eventually, Swiggy patched the loophole — now only *one-time use per device* is allowed, even if using different numbers or accounts.

### 🔴 Zomato Testing

- Discovered a separate loophole: **Zomato initially allowed new accounts using just a new email**, even before linking a mobile number.
- Created a new email → signed up → linked the *same old phone number* → was still treated as a new user.
- Repeated the process using different email IDs and phones to gain first-time user benefits again and again.
- Zomato eventually patched this by linking promotional eligibility more tightly to device & number history.

---

## 📊 Key Findings

| Platform | Initial Loophole | Patch Implemented |
|----------|------------------|-------------------|
| Swiggy   | Reused mobile number with new account still gave first-time coupon | Tied coupon logic to **device ID + number** |
| Zomato   | New email + same number still triggered new user offer | Tied offer logic to **device + number + account history** |

---

## 📚 Skills Demonstrated

- System analysis
- Behavioral testing
- Pattern recognition
- Ethical hacking awareness
- Documentation of evolving app behavior

---

## 🧭 Ethical Reflection

All research was conducted for **educational purposes only**.  
This project was not used to harm or exploit any platform.  
The intent was to understand how real-world platforms function and improve their offer logic — and to reflect on how such weaknesses can be found, tested, and responsibly disclosed.

---

## 🧩 Possible Improvements (for Platforms)

- Use of stronger device fingerprinting
- Tie offer logic to a combination of email, SIM ID, IP history, and device tokens
- Implement better tracking of previously deleted accounts

---

## 🧑‍💻 About Me

I’m a curious learner and a Computer Science graduate who enjoys analyzing real-world systems, finding behavioral patterns, and thinking critically about how platforms are built.

If given an opportunity, I’d love to contribute to QA, growth, or systems testing roles — especially where smart observation is valued over just academic background.

---

## 📫 Contact

Feel free to reach out if you're interested in my approach or thinking style.

tanisharajpal231@gmail.com
tanisharajpal2021@vitbhopal.ac.in



