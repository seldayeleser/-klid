# -klid
import math

# 2D uzaydaki noktaları temsil eden liste
points = [(1, 2), (4, 6), (7, 8), (10, 12)]

# Öklid mesafesi hesaplayan fonksiyon
def euclideanDistance(point1, point2):
    x1, y1 = point1
    x2, y2 = point2
    return math.sqrt((x2 - x1)**2 + (y2 - y1)**2)

# Mesafeleri saklayacak liste
distances = []

# Her nokta çifti arasındaki mesafeyi hesaplama
for i in range(len(points)):
    for j in range(i + 1, len(points)):
        distance = euclideanDistance(points[i], points[j])
        distances.append(distance)

# Minimum mesafeyi bulma ve yazdırma
min_distance = min(distances)
print("Minimum mesafe:", min_distance)
