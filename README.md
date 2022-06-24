#K번째수

def solution(array, commands):
    answer = []
    result = []
    for i in range(len(commands)):
        result.extend(array[(commands[i][0]) - 1: commands[i][1]])
        result.sort()
        answer.append(result[commands[i][2] - 1])
        result.clear()
    return answer


print(solution([1, 5, 2, 6, 3, 7, 4], [[2, 5, 3], [4, 4, 1], [1, 6, 3]]))
