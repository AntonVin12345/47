#include <gtest/gtest.h>
#include <vector>

std::vector<int> increase_vector(const std::vector<int>& vector, int n) {
    std::vector<int> result;
    for (int x : vector) {
        result.push_back(x + n);
    }
    return result;
}

TEST(IncreaseVectorTest, BasicTest) {
  std::vector<int> v = {1, 2, 3, 4, 5};
  int n = 2;
  std::vector<int> expected = {3, 4, 5, 6, 7};

  auto result = increase_vector(v, n);
  EXPECT_EQ(result, expected);
}
