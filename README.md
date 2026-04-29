# reputation-riot-logic-lite
A Python-based sentiment analysis tool for identifying 'poachable' restaurant reviews. 

# WiqkedDevelopmentZ - Reputation Riot: The Shield & Poach Engine
# specialized logic for the Amarillo restaurant scene

def reputation_shield(review_text):
    # These keywords trigger an automatic "Red Alert" to stop a city inspection
    shield_triggers = ["poison", "sick", "hospital", "stomach", "dirty", "gross", "health"]
    
    # These keywords identify a "Poachable" customer from a competitor
    poach_triggers = ["wait", "cold", "rude", "expensive", "never again", "slow"]

    # Convert to lowercase to catch everything
    scan = review_text.lower()

    # 1. THE SHIELD LOGIC (Defense)
    if any(word in scan for word in shield_triggers):
        return "🛡️ SHIELD ACTIVATE: Critical health risk detected. Immediate triage required."

    # 2. THE POACH LOGIC (Offense)
    elif any(word in scan for word in poach_triggers):
        return "🎯 POACH ALERT: Customer is unhappy with service/price. Deploy offer now."

    # 3. STANDARD MONITORING
    else:
        return "👀 MONITORING: Sentiment is stable. No immediate action."

# --- LIVE TEST EXAMPLES ---
print("Test 1 (The Shield):", reputation_shield("I got sick after eating the tacos."))
print("Test 2 (The Poach):", reputation_shield("The service was so slow, I waited an hour."))
