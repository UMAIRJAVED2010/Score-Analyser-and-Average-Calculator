# Score-Analyser-and-Average-Calculator
This project gives the average of scores you write here
# Sports Score Tracker
def calculate_stats(scores):
    if not scores:
        return 0, 0
    average = sum(scores) / len(scores)
    highest = max(scores)
    return average, highest

# Main program
print("--- Sports Performance Tracker ---")
scores = []
while True:
    score = input("Enter score (or type 'done' to finish): ")
    if score.lower() == 'done':
        break
    scores.append(float(score))

if scores:
    avg, high = calculate_stats(scores)
    print(f"\nResults:")
    print(f"Total Matches: {len(scores)}")
    print(f"Average Score: {avg:.2f}")
    print(f"Highest Score: {high}")
else:
    print("No scores entered.")
