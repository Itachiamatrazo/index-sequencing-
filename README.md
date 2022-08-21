# index-sequencing-
Used for sorting the elements 
#include <iostream>
using namespace std;

void indexedSequentialSearch(int arr[], int n, int k)
{
	int elements[20], indices[20], temp, I;
	int i = 0, ind = 0, start, end;
	for (i = 0; i < n; i += 3)
	{
		elements[ind] = arr[i]; // Storing element
		indices[ind] = i;		// Storing the index
		ind++;
	}
	if (k < elements[0])
	{
		printf("not found");
		exit(0);
	}
	else
	{
		for (i = 1; i <= ind; i++)
			if (k < elements[i])
			{
				start = indices[i - 1];
				end = indices[i];
				break;
			}
	}

	for (i = start; i <= end; i++)

	{
		if (k == arr[i])

		{
			int j = 1;

			break;
		}
	}

	int j = 1;
	if (j == 1)

		printf("Found at index %d", i);

	else

		printf("Not found");
}

int main()
{
	int n, k, i;
	cout << "entre the number of the ellements to to sorted " << endl;
	cin >> n;
	int arr[n];
	for (i = 0; i < n; i++)
	{
		cout << "entre the elements" << i + 1 << endl;
		cin >> arr[i];
	}
	cin >> k;

	indexedSequentialSearch(arr, n, k);

	return 0;
