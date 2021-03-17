# About
ROW와 COLUMN의 수를 사용자의 입력을 통해 설정하고, ROW x COLUMN 크기의 게임판을 출력하기
# Mission (Optional)
Subroutine(GOSUB)을 사용하여 게임판의 행,열을 출력하기
# Implementation
```
10 PRINT "LET'S MAKE GAME BOARD WHICH SIZE IS 'ROW X COLUMN'",""
20 INPUT "* ENTER NUM OF ROW: ";ROW : INPUT "* ENTER NUM OF COLUMN: ";COL
30 GOSUB 200

100 END
200 REM print num of rows
210 LET RCNT = 0
220 RCNT = RCNT + 1
230 LET A$ = "+---" : GOSUB 400
240 LET A$ = "|   " : GOSUB 400
250 IF (RCNT < ROW) GOTO 220
260 LET A$ = "+---" : GOSUB 400
300 RETURN

400 REM print num of columns
410 LET CSTR$ = A$ : LET CCNT = 0
430 CCNT = CCNT + 1
440 IF (CCNT < COL) THEN CSTR$ = CSTR$ + A$ : GOTO 430
450 CSTR$ = CSTR$ + LEFT$(A$, 1)
460 PRINT CSTR$
500 RETURN
```
# Result
![image](https://user-images.githubusercontent.com/36250213/111514506-27a60280-8795-11eb-9e2a-b282888ab544.png)
