typedef pair<int, int> ii;
bool cmp(ii a, ii b) { return a.Y < b.Y; }
int maxArea(std::vector<int> a) {
    int n = a.size();

    vector<ii> b;
    for (int i = 0; i < n; i++)
        b.push_back({i, a[i]});

    sort(b.begin(), b.end(), cmp);

    int imax = b[n - 1].X, imin = b[n - 1].X;
    int res = 0;
    for(int i = n - 2; i >= 0; i--) {
        res = max(res, b[i].Y * abs(imax - b[i].X));
        res = max(res, b[i].Y * abs(imin - b[i].X));
        imax = max(b[i].X, imax);
        imin = min(b[i].X, imin);
    }
    return res;
}
