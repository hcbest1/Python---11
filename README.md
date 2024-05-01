# Python---11

{
  "nbformat": 4,
  "nbformat_minor": 0,
  "metadata": {
    "colab": {
      "provenance": [],
      "authorship_tag": "ABX9TyNWe6UGsWkWTkX+0/gDWo6U",
      "include_colab_link": true
    },
    "kernelspec": {
      "name": "python3",
      "display_name": "Python 3"
    },
    "language_info": {
      "name": "python"
    }
  },
  "cells": [
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "view-in-github",
        "colab_type": "text"
      },
      "source": [
        "<a href=\"https://colab.research.google.com/github/ciellleen/copyright/blob/main/11%EC%B0%A8%EC%8B%9C\" target=\"_parent\"><img src=\"https://colab.research.google.com/assets/colab-badge.svg\" alt=\"Open In Colab\"/></a>"
      ]
    },
    {
      "cell_type": "code",
      "execution_count": 4,
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 193
        },
        "id": "tPx6qKQLB_DS",
        "outputId": "068709e7-f26e-477e-d6d6-403ec45fc1b7"
      },
      "outputs": [
        {
          "output_type": "error",
          "ename": "FileNotFoundError",
          "evalue": "[Errno 2] No such file or directory: 'e:/python/Day10/newfile.txt'",
          "traceback": [
            "\u001b[0;31m---------------------------------------------------------------------------\u001b[0m",
            "\u001b[0;31mFileNotFoundError\u001b[0m                         Traceback (most recent call last)",
            "\u001b[0;32m<ipython-input-4-3d9e554ccaef>\u001b[0m in \u001b[0;36m<cell line: 4>\u001b[0;34m()\u001b[0m\n\u001b[1;32m      2\u001b[0m \u001b[0mf\u001b[0m\u001b[0;34m.\u001b[0m\u001b[0mclose\u001b[0m\u001b[0;34m(\u001b[0m\u001b[0;34m)\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n\u001b[1;32m      3\u001b[0m \u001b[0;34m\u001b[0m\u001b[0m\n\u001b[0;32m----> 4\u001b[0;31m \u001b[0mf\u001b[0m \u001b[0;34m=\u001b[0m \u001b[0mopen\u001b[0m\u001b[0;34m(\u001b[0m\u001b[0;34m\"e:/python/Day10/newfile.txt\"\u001b[0m\u001b[0;34m,\u001b[0m \u001b[0;34m'w'\u001b[0m\u001b[0;34m)\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n\u001b[0m\u001b[1;32m      5\u001b[0m \u001b[0mf\u001b[0m\u001b[0;34m.\u001b[0m\u001b[0mclose\u001b[0m\u001b[0;34m(\u001b[0m\u001b[0;34m)\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n",
            "\u001b[0;31mFileNotFoundError\u001b[0m: [Errno 2] No such file or directory: 'e:/python/Day10/newfile.txt'"
          ]
        }
      ],
      "source": [
        "f = open(\"newfile.txt\", 'w')\n",
        "f.close()\n",
        "\n",
        "f = open(\"e:/python/Day10/newfile.txt\", 'w')\n",
        "f.close()"
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "# w: 쓰기\n",
        "f = open('ex_memo.txt','w')\n",
        "students = ['김철수', '최영', '한석규', '김태희']\n",
        "for student in students:\n",
        "    msg = student\n",
        "    f.write(msg+\"\\n\")\n",
        "f.close()\n",
        "\n",
        "\n",
        "\n",
        "file = open('hello.txt', 'w')    # hello.txt 파일을 쓰기 모드(w)로 열기. 파일 객체 반환\n",
        "file.write('Hello, world!')      # 파일에 문자열 저장\n",
        "file.close()"
      ],
      "metadata": {
        "id": "LOKI1koQC6Q9"
      },
      "execution_count": 6,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": [
        "# a: 쓰기\n",
        "f = open('test.txt','a', encoding='UTF-8')\n",
        "\n",
        "for i in range(4,10):\n",
        "    data = \"%d 번째 줄입니다. \\n\"%i\n",
        "    f.write(data)\n",
        "f.close()"
      ],
      "metadata": {
        "id": "YNmYc9l0C6TR"
      },
      "execution_count": 8,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": [
        "dict1 = {'hello' : 1, 'brother' : 2}\n",
        "file1 = open(\"Original.txt\", \"w\")\n",
        "\n",
        "str1 = repr(dict1)\n",
        "file1.write(\"dict1 = \" + str1 + \"\\n\")\n",
        "\n",
        "file1.close()\n",
        "test_file = open(\"test.txt\",\"w\")\n",
        "\n",
        "a = 1\n",
        "b = 2\n",
        "test_file.write('%d + %d = %d' %(a, b, a+b))\n",
        "\n",
        "test_file.close\n"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "8ERwoUwCDTLk",
        "outputId": "aaa5880b-a116-4608-9526-64d8fc26cf13"
      },
      "execution_count": 9,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "<function TextIOWrapper.close()>"
            ]
          },
          "metadata": {},
          "execution_count": 9
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "from random import randint  #난수 생성 랜덤 int를 가져옴\n",
        "\n",
        "\n",
        "with open('text.txt', 'w') as f:\n",
        "   f.write('이번주 로또 번호는 ->')\n",
        "   for lotto in range(6):\n",
        "      f.write(str(randint(0,50)) +' , ')\n",
        "\n",
        "f.close()"
      ],
      "metadata": {
        "id": "Sjuhm00MDTOB"
      },
      "execution_count": 11,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": [
        "lines = ['안녕하세요.\\n', '파이썬\\n', '코딩 도장입니다.\\n']\n",
        "\n",
        "with open('hello.txt', 'w') as file:\n",
        "# hello.txt 파일을 쓰기 모드(w)로 열기\n",
        "    file.writelines(lines)\n",
        "file.close()\n",
        "\n",
        "f = open(\"hz.txt\", \"a\", encoding='UTF-8')\n",
        "\n",
        "f.writelines([\"\\n홈짱닷컴\", \"\\nHomzzang.com\"])\n",
        "\n",
        "f.close()"
      ],
      "metadata": {
        "id": "gaA2qnhRDTQe"
      },
      "execution_count": 14,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": [
        "# w: 쓰기\n",
        "f = open('ex_memo1.txt','w')\n",
        "students = ['김철수', '최영', '한석규', '김태희']\n",
        "for student in students:\n",
        "    msg = student\n",
        "    f.write(msg+\"\\n\")\n",
        "f.close()\n",
        "\n",
        "\n",
        "f = open('ex_memo2.txt','w')\n",
        "students = ['김철수', '최영', '한석규', '김태희']\n",
        "f.writelines('\\n'.join(students))\n",
        "f.close()"
      ],
      "metadata": {
        "id": "K99euXSBENLt"
      },
      "execution_count": 16,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": [
        "#파일 r 모드로 열기\n",
        "f = open('t2.txt','r')\n",
        "\n",
        "# read() 함수 이용해서 하나씩 읽어오기\n",
        "print('\\n1. read()')\n",
        "print(f'위치 : {f.tell()}')\n",
        "\n",
        "s1 = f.read(1)\n",
        "print(s1)\n",
        "\n",
        "# readline() 함수 이용해서 한 라인씩 읽어오기\n",
        "print('\\n2. readline()')\n",
        "print(f'위치 : {f.tell()}')\n",
        "\n",
        "s2 = f.readline()\n",
        "print(s2)\n",
        "\n",
        "# readlines() 함수 이용해서 모두 읽어오기\n",
        "print('\\n3. readlines()')\n",
        "print(f'위치 : {f.tell()}')\n",
        "\n",
        "s3 = f.readlines()\n",
        "print(s3)"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 211
        },
        "id": "D0NMt8dWENOA",
        "outputId": "396667e3-d741-4c14-eb8c-d49e1678a153"
      },
      "execution_count": 22,
      "outputs": [
        {
          "output_type": "error",
          "ename": "FileNotFoundError",
          "evalue": "[Errno 2] No such file or directory: 't2.txt'",
          "traceback": [
            "\u001b[0;31m---------------------------------------------------------------------------\u001b[0m",
            "\u001b[0;31mFileNotFoundError\u001b[0m                         Traceback (most recent call last)",
            "\u001b[0;32m<ipython-input-22-25868fd5e094>\u001b[0m in \u001b[0;36m<cell line: 2>\u001b[0;34m()\u001b[0m\n\u001b[1;32m      1\u001b[0m \u001b[0;31m#파일 r 모드로 열기\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n\u001b[0;32m----> 2\u001b[0;31m \u001b[0mf\u001b[0m \u001b[0;34m=\u001b[0m \u001b[0mopen\u001b[0m\u001b[0;34m(\u001b[0m\u001b[0;34m't2.txt'\u001b[0m\u001b[0;34m,\u001b[0m\u001b[0;34m'r'\u001b[0m\u001b[0;34m)\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n\u001b[0m\u001b[1;32m      3\u001b[0m \u001b[0;34m\u001b[0m\u001b[0m\n\u001b[1;32m      4\u001b[0m \u001b[0;31m# read() 함수 이용해서 하나씩 읽어오기\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n\u001b[1;32m      5\u001b[0m \u001b[0mprint\u001b[0m\u001b[0;34m(\u001b[0m\u001b[0;34m'\\n1. read()'\u001b[0m\u001b[0;34m)\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n",
            "\u001b[0;31mFileNotFoundError\u001b[0m: [Errno 2] No such file or directory: 't2.txt'"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "#파일 r 모드로 열기\n",
        "f = open(r'text.txt')\n",
        "#f = open('text.txt', 'r')\n",
        "#디폴트 인코딩 cp949\n",
        "\n",
        "text = f.read() #파일의 내용 전체를 문자열로 리턴\n",
        "print(text)\n",
        "\n",
        "f.close()\n"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "26RfZRYFFx7H",
        "outputId": "94e66b0e-4b13-4b08-cbf9-32fd1a471c1c"
      },
      "execution_count": 25,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "이번주 로또 번호는 ->39 , 24 , 6 , 32 , 49 , 42 , \n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "#파일 r 모드로 열기\n",
        "f = open(r'test.txt')\n",
        "line = f.readline() #파일의 라인 끝에 줄 바꿈 (\\n) 이 있을 경우 줄바꿈을 포함합니다.\n",
        "line = line.strip() #줄 바꿈 (\\n) 제거\n",
        "print(line) #1번째 줄입니다.\n",
        "line = f.readline()\n",
        "line = line.strip()\n",
        "print(line) #2번째 줄입니다.\n",
        "line = f.readline()\n",
        "line = line.strip()\n",
        "print(line) #3번째 줄입니다.\n",
        "\n",
        "f.close()"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "IH3UbDlbFx9L",
        "outputId": "9927d42c-fd25-4ee4-f660-fbced9d50dd3"
      },
      "execution_count": 31,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "\n",
            "\n",
            "\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "#파일 r 모드로 열기\n",
        "f = open(r'text.txt')\n",
        "\n",
        "# 맨 처음 위치로 가서 한줄 읽기\n",
        "print('\\n4. seek(0), readline()')\n",
        "\n",
        "f.seek(0)\n",
        "print(f'위치 : {f.tell()}')\n",
        "\n",
        "s4 = f.readline()\n",
        "print(s4)\n",
        "\n",
        "\n",
        "# 파일 닫기\n",
        "f.close()\n"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "GOTOSTdgGcfg",
        "outputId": "c4b34dfc-fe02-4db3-9b04-2ad316f478d4"
      },
      "execution_count": 32,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "\n",
            "4. seek(0), readline()\n",
            "위치 : 0\n",
            "이번주 로또 번호는 ->39 , 24 , 6 , 32 , 49 , 42 , \n"
          ]
        }
      ]
    }
  ]
}
