#include <string>
#include <vector>

using namespace std;

int solution(vector<int> queue1, vector<int> queue2) {
    int answer{};

    long long sumQ1{};
    long long sumQ2{};
    int size{ static_cast<int>(queue1.size()) };
    for (int i = 0; i < queue1.size(); i++)
    {
        sumQ1 += queue1[i];
        sumQ2 += queue2[i];
    }
    if ((sumQ1 + sumQ2) % 2 == 1)
    {
        return -1;
    }
    int strQ1{};
    int strQ2{};
    while (true)
    {
        if (strQ1 > size && strQ2 > size)
        {
            return -1;
        }
        if (sumQ1 == sumQ2)
        {
            break;
        }
        else if (sumQ1 > sumQ2)
        {
            if (strQ1 == queue1.size() - 1)
            {
                return -1;
            }
            sumQ1 -= queue1[strQ1];
            queue2.push_back(queue1[strQ1]);
            sumQ2 += queue1[strQ1++];

        }
        else
        {
            if (strQ2 == queue2.size() - 1)
            {
                return -1;
            }
            sumQ2 -= queue2[strQ2];
            queue1.push_back(queue2[strQ2]);
            sumQ1 += queue2[strQ2++];
        }
        answer++;
    }

    return answer;
}