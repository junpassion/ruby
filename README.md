ruby
====

share  the knowledge 

//this   is for two matrixes to multiply  P m*n   Q：n*s //
void M_Mult(float *t, float *p, float *q, int m, int n, int s)
{
	int i, j, k;
	float *temp = t, *temp1 = p, * temp2 = q;
	for(i = 0; i < m; i++)
		for(j = 0; j < s; j++)
		{
			float t = 0;
			for(k = 0; k < n; k++)
			{
				temp1 = p + i*n;
				temp2 = q +j;
				t += (*(temp1+k))*(*(temp2+k*s));
			}
			*temp++ = t;
		}
}
