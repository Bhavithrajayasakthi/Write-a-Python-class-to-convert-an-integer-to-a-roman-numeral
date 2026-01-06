# Write-a-Python-class-to-convert-an-integer-to-a-roman-numeral
class RomanSolution:
    @staticmethod
    def int_to_Roman(num):
        val = [1000, 900, 500, 400, 100, 90, 50, 40, 10, 9, 5, 4, 1]
        syb = ["M", "CM", "D", "CD", "C", "XC", "L", "XL", "X", "IX", "V", "IV", "I"]

        roman_num = ""
        i = 0

        if num < 1 or num > 3999:
            return "ENTER A GOOD VALUE!"

        while num > 0:
            if num >= val[i]:
                roman_num += syb[i]
                num -= val[i]
            else:
                i += 1

        return roman_num


n = int(input("ENTER A NUMBER: "))
print("Roman numeral of given number is:", RomanSolution.int_to_Roman(n))
output
ENTER A NUMBER: 58
Roman numeral of given number is: LVIII

