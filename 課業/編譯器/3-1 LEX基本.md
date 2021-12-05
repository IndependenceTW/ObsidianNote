## 基本語法
``` c
// Definition section
%%
// Rules section
%%
// Subroutine section
```

Example:
``` c
%{
// write some C code here
unsigned int charCount=0, wordCount=0, lineCount=0;
%}
word [^ \t\n]+
eol \n
// write some RE definition here
%%
{word} { wordCount++; charCount += yyleng; }
{eol} { charCount++; lineCount++; }
. charCount++;
// write some rules here
%%
int main(int argc, char *argv[]) {
 yylex();
 printf("%u %u %u\n", lineCount, wordCount, charCount);
 return(0);
}
// write some c code here
```

%% Comment 待補 %%

## Regular Expression
![[Pasted image 20211201100148.png]]
![[Pasted image 20211201100201.png]]