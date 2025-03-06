
from collections import deque

def bfs_shortest_path(adj_matrix, start, end):
    # Проверка на корректность ввода
    if start < 0 or start >= len(adj_matrix) or end < 0 or end >= len(adj_matrix)):
        return None

    # Очередь для BFS
    queue = deque()
    queue.append((start, [start]))

    # Посещенные вершины
    visited = set()
    visited.add(start)

    while queue:
        current, path = queue.popleft()

        # Если достигли целевой вершины, возвращаем путь
        if current == end:
            return path

        # Перебираем соседей
        for neighbor in range(len(adj_matrix)):
            if adj_matrix[current][neighbor] == 1 and neighbor not in visited:
                visited.add(neighbor)
                queue.append((neighbor, path + [neighbor]))

    # Если путь не найден
    return None

def main():
    # Ввод матрицы смежности
    n = int(input("Введите количество вершин графа: "))
    print("Введите матрицу смежности (построчно, элементы разделяйте пробелами):")
    adj_matrix = []
    for _ in range(n):
        row = list(map(int, input().split()))
        adj_matrix.append(row)

    # Ввод начальной и целевой вершин
    start = int(input("Введите начальную вершину: "))
    end = int(input("Введите целевую вершину: "))

    # Поиск пути
    path = bfs_shortest_path(adj_matrix, start, end)

    # Вывод результата
    if path:
        print(f"Путь от вершины {start} до вершины {end}: {' -> '.join(map(str, path))}")
    else:
        print(f"Путь от вершины {start} до вершины {end} не найден.")

if __name__ == "__main__":
    main()