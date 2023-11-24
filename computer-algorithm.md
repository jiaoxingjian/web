# computer algorithm

## resources

- [PageRank: A Trillion Dollar Algorithm](https://www.youtube.com/watch?v=JGQe4kiPnrU&pp=ygUfY29tcHV0ZXIgYWxnb3JpdGhtIG1hcmtvdiBjaGFpbg%3D%3D)
- [Monte Carlo Simulation](https://www.youtube.com/watch?v=7ESK5SaP-bc&pp=ygUfY29tcHV0ZXIgYWxnb3JpdGhtIG1hcmtvdiBjaGFpbg%3D%3D)
- [Page rank and Markov chain](https://www.youtube.com/watch?v=qBJZabwIZBo&pp=ygUfY29tcHV0ZXIgYWxnb3JpdGhtIG1hcmtvdiBjaGFpbg%3D%3D)
- 

## c++

algorithm的c++实现。

- [ ] [Better Algorithm Intuition - Conor Hoekstra - code::dive 2019](https://www.youtube.com/watch?v=0z-cv3gartw&t=1450s)
  ![](https://i.imgur.com/VLCngwL.png)
  ![](https://i.imgur.com/oD72U4Y.png)
  ![](https://i.imgur.com/biWdqYI.png)
  ![](https://i.imgur.com/pjug9XM.png)
  ![](https://i.imgur.com/7tqdVr1.png)
  ![](https://i.imgur.com/Cu8xZxf.png)
  ![](https://i.imgur.com/QXWRz3N.png)
  ![](https://i.imgur.com/JlyENg6.png)
  ![](https://i.imgur.com/1AqBv2q.png)
  ![](https://i.imgur.com/iRKDhE9.png)
  ![](https://i.imgur.com/uK8SVvR.png)
  ![](https://i.imgur.com/BJqbKAq.png)
  ![](https://i.imgur.com/qaY13Aj.png)

> next level file system





# basic

```
#include <algorithm>
#include <array>
#include <iostream>
 
int main()
{
    const auto v = {1, 2, 3, 4};
 
    for (int n : {3, 5})
        (std::find(v.begin(), v.end(), n) == std::end(v))
            ? std::cout << "v does not contain " << n << '\n'
            : std::cout << "v contains " << n << '\n';
 
    auto is_even = [](int i) { return i % 2 == 0; };
 
    for (auto const& w : {std::array{3, 1, 4}, {1, 3, 5}})
        if (auto it = std::find_if(begin(w), end(w), is_even); it != std::end(w))
            std::cout << "w contains an even number " << *it << '\n';
        else
            std::cout << "w does not contain even numbers\n";
}
Output:

v contains 3
v does not contain 5
w contains an even number 4
w does not contain even numbers
```



```
#include <algorithm>
#include <array>
#include <iostream>
#include <iterator>
 
int main()
{
    constexpr std::array v {1, 2, 3, 4, 4, 3, 7, 8, 9, 10};
    std::cout << "v: ";
    std::copy(v.cbegin(), v.cend(), std::ostream_iterator<int>(std::cout, " "));
    std::cout << '\n';
 
    // determine how many integers match a target value.
    for (const int target: {3, 4, 5})
    {
        const int num_items = std::count(v.cbegin(), v.cend(), target);
        std::cout << "number: " << target << ", count: " << num_items << '\n';
    }
 
    // use a lambda expression to count elements divisible by 4.
    int count_div4 = std::count_if(v.begin(), v.end(), [](int i) { return i % 4 == 0; });
    std::cout << "numbers divisible by four: " << count_div4 << '\n';
 
    // A simplified version of `distance` with O(N) complexity:
    auto distance = [](auto first, auto last)
    {
        return std::count_if(first, last, [](auto) { return true; });
    };
    static_assert(distance(v.begin(), v.end()) == 10);
}
Output:

v: 1 2 3 4 4 3 7 8 9 10
number: 3, count: 2
number: 4, count: 2
number: 5, count: 0
numbers divisible by four: 3
```

```

#include <iostream>
#include <vector>
#include <algorithm>

int main() {
    std::vector<int> numbers = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};

    // Print the original vector
    std::cout << "Original Vector: ";
    for (int num : numbers) {
        std::cout << num << " ";
    }
    std::cout << std::endl;

    // Remove the number 5 from the vector
    numbers.erase(std::remove(numbers.begin(), numbers.end(), 5), numbers.end());

    // Print the modified vector
    std::cout << "Modified Vector: ";
    for (int num : numbers) {
        std::cout << num << " ";
    }
    std::cout << std::endl;

    return 0;
}
```



```

#include <iostream>
#include <vector>
#include <algorithm>

bool isEven(int num) {
    return num % 2 == 0;
}

int main() {
    std::vector<int> numbers = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};

    // Print the original vector
    std::cout << "Original Vector: ";
    for (int num : numbers) {
        std::cout << num << " ";
    }
    std::cout << std::endl;

    // Remove all even numbers from the vector
    numbers.erase(std::remove_if(numbers.begin(), numbers.end(), isEven), numbers.end());

    // Print the modified vector
    std::cout << "Modified Vector: ";
    for (int num : numbers) {
        std::cout << num << " ";
    }
    std::cout << std::endl;

    return 0;
}
```

```
#include <algorithm>
#include <array>
#include <functional>
#include <iostream>
 
int main()
{
    std::array<int, 10> s {5, 7, 4, 2, 8, 6, 1, 9, 0, 3};
 
    std::replace(s.begin(), s.end(), 8, 88);
 
    for (int a : s)
        std::cout << a << ' ';
    std::cout << '\n';
 
    std::replace_if(s.begin(), s.end(), 
                    std::bind(std::less<int>(), std::placeholders::_1, 5), 55);
 
    for (int a : s)
        std::cout << a << ' ';
    std::cout << '\n';
}
Output:

5 7 4 2 88 6 1 9 0 3
5 7 55 55 88 6 55 9 55 55
```

![image-20230716112557948](.\Img\image-20230716112557948.png)



![image-20230716112629584](.\Img\image-20230716112629584.png)











![image-20230716113700714](.\Img\image-20230716113700714.png)



![image-20230716112712308](.\Img\image-20230716112712308.png)







![image-20230716112738733](.\Img\image-20230716112738733.png)



![image-20230716112758431](.\Img\image-20230716112758431.png)



![image-20230716113337776](.\Img\image-20230716113337776.png)



```

```

![image-20230716112314817](.\Img\image-20230716112314817.png)





![image-20230716112412646](.\Img\image-20230716112412646.png)