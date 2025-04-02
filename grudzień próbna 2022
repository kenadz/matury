def zadanie_1_1(match_result): count = sum(1 for i in range(1, len(match_result)) if match_result[i] != match_result[i - 1]) return count

def zadanie_1_2(match_result): score_A, score_B = 0, 0 for i, char in enumerate(match_result): if char == 'A': score_A += 1 else: score_B += 1 if (score_A >= 1000 or score_B >= 1000) and abs(score_A - score_B) >= 3: winner = 'A' if score_A > score_B else 'B' return f"{winner} {score_A}:{score_B}" return "Set not finished"

def zadanie_1_3(match_result): max_streak = 0 total_streaks = 0 current_streak = 1 longest_streak_team = ''

for i in range(1, len(match_result)):
    if match_result[i] == match_result[i - 1]:
        current_streak += 1
    else:
        if current_streak >= 10:
            total_streaks += 1
            if current_streak > max_streak:
                max_streak = current_streak
                longest_streak_team = match_result[i - 1]
        current_streak = 1

if current_streak >= 10:
    total_streaks += 1
    if current_streak > max_streak:
        max_streak = current_streak
        longest_streak_team = match_result[-1]

return total_streaks, max_streak, longest_streak_team

with open("mecz.txt", "r") as file: match_result = file.read().strip()

with open("wyniki1.txt", "w") as output: output.write(f"1.1 {zadanie_1_1(match_result)}\n") output.write(f"1.2 {zadanie_1_2(match_result)}\n") streaks, max_streak, team = zadanie_1_3(match_result) output.write(f"1.3 {streaks} {max_streak} {team}\n")

