CCI-150
=======

Coding solutions for Cracking the Coding Interview 

1.1 Implement an algorithm to determine if a string has all unique characters. What if you can not use additional data structures?

bool uniqueString(string s)
{
  bool a[256];
  memset(a,0,sizeof(a));
  int len = s.lengeth();
  for (int i=0; i< len; ++i)
  {
    int v = (int)s[i];
    if(a[v])
    return false;
    a[v] = true;
  }
  return true;
}
