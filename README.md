The easiest way to do UI Automation.

Attention:

    no trojan, no backdoor...

Interface:

    BOOL op(PCWSTR, PCWSTR);
    BOOL sp(PCWSTR, PCWSTR);
    BOOL fp(PCWSTR, PCWSTR, LONG*, LONG*);
    BOOL sc(LONG, LONG); //single click
    BOOL dc(LONG, LONG); //double click
    BOOL mc(LONG, LONG); //middle click
    BOOL rc(LONG, LONG); //right click

Sample code:

    #pragma comment(lib,"F:\Public\\sm.lib")

    int main()
    {
        LONG x, y;

        if (op(L"无标题 - 画图", NULL)
            return TRUE;

        while (!fp(L"xxx", L"xxx", &x, &y)
            && fp(L"向下翻页", L"按钮", &x, &y))
        {
            sc(x, y);
            Sleep(1000);
        }

        dc(x, y);
        return 0;
    }
