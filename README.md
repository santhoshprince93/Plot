# Plot
{
 "cells": [
  {
   "cell_type": "code",
   "execution_count": 1,
   "id": "e4c029a2",
   "metadata": {},
   "outputs": [],
   "source": [
    "import matplotlib.pyplot as plt"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 3,
   "id": "abe8e83b",
   "metadata": {},
   "outputs": [],
   "source": [
    "x = [-3,5,7]"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 4,
   "id": "c18c8bbc",
   "metadata": {},
   "outputs": [],
   "source": [
    "y = [10,2,5]"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 13,
   "id": "3b99e557",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "Text(0.5, 1.03, 'Sales Comparision')"
      ]
     },
     "execution_count": 13,
     "metadata": {},
     "output_type": "execute_result"
    },
    {
     "data": {
      "image/png": "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\n",
      "text/plain": [
       "<Figure size 1080x216 with 1 Axes>"
      ]
     },
     "metadata": {
      "needs_background": "light"
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "fig = plt.figure(figsize=(15,3))\n",
    "plt.plot(x, y)\n",
    "plt.xlim(-4, 10)\n",
    "plt.ylim(-3, 12)\n",
    "plt.xlabel('X Axis')\n",
    "plt.ylabel('Y Axis')\n",
    "plt.title('line Plot')\n",
    "plt.suptitle('Sales Comparision', size=20, y=1.03)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 14,
   "id": "c22645f9",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([15.,  3.])"
      ]
     },
     "execution_count": 14,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "fig.get_size_inches()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 15,
   "id": "f0aeac1b",
   "metadata": {},
   "outputs": [],
   "source": [
    "fig.set_size_inches(14,4)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 16,
   "id": "20b6abb7",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "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\n",
      "text/plain": [
       "<Figure size 1008x288 with 1 Axes>"
      ]
     },
     "execution_count": 16,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "fig"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 19,
   "id": "76efec8a",
   "metadata": {},
   "outputs": [],
   "source": [
    "import pandas as pd\n",
    "import numpy as np"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 20,
   "id": "c3a9944d",
   "metadata": {},
   "outputs": [],
   "source": [
    "df = pd.read_csv(\"salaries.csv\")"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 21,
   "id": "13212cb3",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>rank</th>\n",
       "      <th>discipline</th>\n",
       "      <th>phd</th>\n",
       "      <th>service</th>\n",
       "      <th>sex</th>\n",
       "      <th>salary</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>Prof</td>\n",
       "      <td>B</td>\n",
       "      <td>56</td>\n",
       "      <td>49</td>\n",
       "      <td>Male</td>\n",
       "      <td>186960</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>Prof</td>\n",
       "      <td>A</td>\n",
       "      <td>12</td>\n",
       "      <td>6</td>\n",
       "      <td>Male</td>\n",
       "      <td>93000</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>Prof</td>\n",
       "      <td>A</td>\n",
       "      <td>23</td>\n",
       "      <td>20</td>\n",
       "      <td>Male</td>\n",
       "      <td>110515</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>Prof</td>\n",
       "      <td>A</td>\n",
       "      <td>40</td>\n",
       "      <td>31</td>\n",
       "      <td>Male</td>\n",
       "      <td>131205</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>Prof</td>\n",
       "      <td>B</td>\n",
       "      <td>20</td>\n",
       "      <td>18</td>\n",
       "      <td>Male</td>\n",
       "      <td>104800</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "   rank discipline  phd  service   sex  salary\n",
       "0  Prof          B   56       49  Male  186960\n",
       "1  Prof          A   12        6  Male   93000\n",
       "2  Prof          A   23       20  Male  110515\n",
       "3  Prof          A   40       31  Male  131205\n",
       "4  Prof          B   20       18  Male  104800"
      ]
     },
     "execution_count": 21,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df.head()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 23,
   "id": "505ee9b0",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "Index(['rank', 'discipline', 'phd', 'service', 'sex', 'salary'], dtype='object')"
      ]
     },
     "execution_count": 23,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df.columns"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 24,
   "id": "81f9116f",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(78, 6)"
      ]
     },
     "execution_count": 24,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df.shape"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 27,
   "id": "217122ea",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th>phd</th>\n",
       "      <th>1</th>\n",
       "      <th>2</th>\n",
       "      <th>3</th>\n",
       "      <th>4</th>\n",
       "      <th>5</th>\n",
       "      <th>7</th>\n",
       "      <th>8</th>\n",
       "      <th>9</th>\n",
       "      <th>10</th>\n",
       "      <th>11</th>\n",
       "      <th>...</th>\n",
       "      <th>30</th>\n",
       "      <th>33</th>\n",
       "      <th>35</th>\n",
       "      <th>36</th>\n",
       "      <th>38</th>\n",
       "      <th>39</th>\n",
       "      <th>40</th>\n",
       "      <th>45</th>\n",
       "      <th>51</th>\n",
       "      <th>56</th>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>service</th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>1</td>\n",
       "      <td>2</td>\n",
       "      <td>0</td>\n",
       "      <td>1</td>\n",
       "      <td>1</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>...</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>1</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>...</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>3</td>\n",
       "      <td>0</td>\n",
       "      <td>1</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>...</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>1</td>\n",
       "      <td>1</td>\n",
       "      <td>1</td>\n",
       "      <td>0</td>\n",
       "      <td>2</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>1</td>\n",
       "      <td>...</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>1</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>...</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>5</th>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>1</td>\n",
       "      <td>0</td>\n",
       "      <td>...</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>6</th>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>1</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>...</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>7</th>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>1</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>...</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>8</th>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>1</td>\n",
       "      <td>0</td>\n",
       "      <td>...</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>9</th>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>...</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>10</th>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>...</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>11</th>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>1</td>\n",
       "      <td>...</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>14</th>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>...</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>15</th>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>...</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>17</th>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>...</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>18</th>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>...</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>19</th>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>...</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>1</td>\n",
       "      <td>1</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>20</th>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>...</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>21</th>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>...</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>22</th>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>...</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>23</th>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>...</td>\n",
       "      <td>1</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>24</th>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>...</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>25</th>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>...</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>26</th>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>...</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>1</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>27</th>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>...</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>30</th>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>...</td>\n",
       "      <td>0</td>\n",
       "      <td>1</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>31</th>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>...</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>1</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>1</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>33</th>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>...</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>1</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>1</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>36</th>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>...</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>1</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>43</th>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>...</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>1</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>45</th>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>...</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>1</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>49</th>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>...</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>1</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>51</th>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>...</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>0</td>\n",
       "      <td>1</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "<p>33 rows × 36 columns</p>\n",
       "</div>"
      ],
      "text/plain": [
       "phd      1   2   3   4   5   7   8   9   10  11  ...  30  33  35  36  38  39  \\\n",
       "service                                          ...                           \n",
       "0         1   2   0   1   1   0   0   0   0   0  ...   0   0   0   0   0   0   \n",
       "1         0   0   1   0   0   0   0   0   0   0  ...   0   0   0   0   0   0   \n",
       "2         0   0   0   3   0   1   0   0   0   0  ...   0   0   0   0   0   0   \n",
       "3         0   0   1   1   1   0   2   0   0   1  ...   0   0   0   0   0   0   \n",
       "4         0   0   0   1   0   0   0   0   0   0  ...   0   0   0   0   0   0   \n",
       "5         0   0   0   0   0   0   0   0   1   0  ...   0   0   0   0   0   0   \n",
       "6         0   0   0   0   0   1   0   0   0   0  ...   0   0   0   0   0   0   \n",
       "7         0   0   0   0   0   0   0   1   0   0  ...   0   0   0   0   0   0   \n",
       "8         0   0   0   0   0   0   0   0   1   0  ...   0   0   0   0   0   0   \n",
       "9         0   0   0   0   0   0   0   0   0   0  ...   0   0   0   0   0   0   \n",
       "10        0   0   0   0   0   0   0   0   0   0  ...   0   0   0   0   0   0   \n",
       "11        0   0   0   0   0   0   0   0   0   1  ...   0   0   0   0   0   0   \n",
       "14        0   0   0   0   0   0   0   0   0   0  ...   0   0   0   0   0   0   \n",
       "15        0   0   0   0   0   0   0   0   0   0  ...   0   0   0   0   0   0   \n",
       "17        0   0   0   0   0   0   0   0   0   0  ...   0   0   0   0   0   0   \n",
       "18        0   0   0   0   0   0   0   0   0   0  ...   0   0   0   0   0   0   \n",
       "19        0   0   0   0   0   0   0   0   0   0  ...   0   0   0   1   1   0   \n",
       "20        0   0   0   0   0   0   0   0   0   0  ...   0   0   0   0   0   0   \n",
       "21        0   0   0   0   0   0   0   0   0   0  ...   0   0   0   0   0   0   \n",
       "22        0   0   0   0   0   0   0   0   0   0  ...   0   0   0   0   0   0   \n",
       "23        0   0   0   0   0   0   0   0   0   0  ...   1   0   0   0   0   0   \n",
       "24        0   0   0   0   0   0   0   0   0   0  ...   0   0   0   0   0   0   \n",
       "25        0   0   0   0   0   0   0   0   0   0  ...   0   0   0   0   0   0   \n",
       "26        0   0   0   0   0   0   0   0   0   0  ...   0   0   0   1   0   0   \n",
       "27        0   0   0   0   0   0   0   0   0   0  ...   0   0   0   0   0   0   \n",
       "30        0   0   0   0   0   0   0   0   0   0  ...   0   1   0   0   0   0   \n",
       "31        0   0   0   0   0   0   0   0   0   0  ...   0   0   1   0   0   0   \n",
       "33        0   0   0   0   0   0   0   0   0   0  ...   0   0   1   0   0   1   \n",
       "36        0   0   0   0   0   0   0   0   0   0  ...   0   0   0   0   0   1   \n",
       "43        0   0   0   0   0   0   0   0   0   0  ...   0   0   0   0   0   0   \n",
       "45        0   0   0   0   0   0   0   0   0   0  ...   0   0   0   0   0   0   \n",
       "49        0   0   0   0   0   0   0   0   0   0  ...   0   0   0   0   0   0   \n",
       "51        0   0   0   0   0   0   0   0   0   0  ...   0   0   0   0   0   0   \n",
       "\n",
       "phd      40  45  51  56  \n",
       "service                  \n",
       "0         0   0   0   0  \n",
       "1         0   0   0   0  \n",
       "2         0   0   0   0  \n",
       "3         0   0   0   0  \n",
       "4         0   0   0   0  \n",
       "5         0   0   0   0  \n",
       "6         0   0   0   0  \n",
       "7         0   0   0   0  \n",
       "8         0   0   0   0  \n",
       "9         0   0   0   0  \n",
       "10        0   0   0   0  \n",
       "11        0   0   0   0  \n",
       "14        0   0   0   0  \n",
       "15        0   0   0   0  \n",
       "17        0   0   0   0  \n",
       "18        0   0   0   0  \n",
       "19        0   0   0   0  \n",
       "20        0   0   0   0  \n",
       "21        0   0   0   0  \n",
       "22        0   0   0   0  \n",
       "23        0   0   0   0  \n",
       "24        0   0   0   0  \n",
       "25        0   0   0   0  \n",
       "26        0   0   0   0  \n",
       "27        0   0   0   0  \n",
       "30        0   0   0   0  \n",
       "31        1   0   0   0  \n",
       "33        0   0   0   0  \n",
       "36        0   0   0   0  \n",
       "43        0   1   0   0  \n",
       "45        0   1   0   0  \n",
       "49        0   0   0   1  \n",
       "51        0   0   1   0  \n",
       "\n",
       "[33 rows x 36 columns]"
      ]
     },
     "execution_count": 27,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "pd.crosstab(df.service,df.phd)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 28,
   "id": "5df4f65e",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "<AxesSubplot:xlabel='phd'>"
      ]
     },
     "execution_count": 28,
     "metadata": {},
     "output_type": "execute_result"
    },
    {
     "data": {
      "image/png": "iVBORw0KGgoAAAANSUhEUgAAAXQAAAI2CAYAAABAG3OpAAAAOXRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjMuNCwgaHR0cHM6Ly9tYXRwbG90bGliLm9yZy8QVMy6AAAACXBIWXMAAAsTAAALEwEAmpwYAAA7TklEQVR4nO3deXhU5d3/8c8dEqBIiIYECAkkLIGErCyCWvoEsSCLqQYEF9pSaVVcHnctT/1ZEauiLY8bFtRKi8UHrYKIggsKKlgpmwQoEAEBCWuAAGHPcv/+yISOY0Im5JwgJ+/Xdc2VmTP3nO89w+TDyck93xhrrQAA576Qsz0BAIAzCHQA8AgCHQA8gkAHAI8g0AHAIwh0APCI0LM9AQBww/Lly1uEhob+RVKqzr2D1zJJa0pKSn7TvXv3PcE+iEAH4EmhoaF/adWqVXJ0dHRhSEjIOfWBm7KyMlNQUNBl165df5H0s2Afd679rwUAwUqNjo4+dK6FuSSFhITY6Ojogyr/6SL4x7k0HwA420LOxTCv4Jt7jTKaQAcAB9x1112tZ82aFX4258A5dAAIUnFxscLCwiq975lnntlRx9P5Ho7QAdQ7hw4dCunTp0/Hzp07d0lMTEx5+eWXL1i4cGGTCy+8sHNKSkpy7969E7du3RomST179ux8++23x1544YWdx4wZExMbG5tWWloqSSoqKgpp1apV+okTJ8zQoUMT/vrXv14gSZ999lmTrl27JnXu3LlLWlpacmFhYUhJSYluvvnmuNTU1OROnTp1+eMf/xjl9PPiCB1AvTNz5sxmrVq1Kv700083StK+ffsa/PSnP02cM2fOxtatW5e8/PLLF9x3332xb7755hZJOnDgQIOlS5fmSdLKlSubzJ07Nzw7O7vo9ddfj8jKyjrYqFGjU+fqjx8/bkaMGNHhtdde25SVlXV0//79IU2bNi175plnoiIiIkrXrFmz7tixY+bCCy9Mys7OPpSUlHTSqedFoAOod7p163bswQcfbHPLLbfEXnnllQebN29esmHDhh/17du3kySVlZUpOjq6uGL8ddddt7/i+rBhwwqnT59+QXZ2dtE//vGPyFtvvbXAf9+rVq1q3KJFi+KsrKyjkhQZGVkmSR9//HGz9evXN5k9e/YFklRUVNRg7dq1jQl0AKiF9PT0EytWrFg7Y8aMiAcffDC2T58+hzp27Hhs5cqV6ysbHx4eXlZx/brrrjswbty42N27dzdYs2ZNk+zs7EP+Y621MsZ8b3WNtdZMmDDh26FDhx4KvM8pnEMHUO9s2bIlLDw8vOzWW2/df9ddd+1etmzZefv37w/9+OOPz5OkEydOmGXLljWu7LERERFlGRkZR26++ea2l1122cHQ0O8eF2dkZBzfvXt3w88++6yJJBUWFoYUFxerX79+BydNmhR94sQJI0mrVq1qdOjQIUczmCN0APXO8uXLf/Q///M/cSEhIQoNDbV//vOft4aGhto77rijbVFRUYPS0lJzyy237O7Ro8fxyh4/fPjwwlGjRrV/77338gLva9y4sX3ttdc23XHHHW2PHz8e0rhx47LPP//867vvvnvvli1bGqWlpSVba01kZGTx3LlzNzn5vAx/gg6AF+Xm5m7JyMjYe7bnURu5ublRGRkZCcGO55QLAHgEgQ4AHkGgA4BHEOgA4BEEOgB4BIEOAB5BoAOAi956661mCQkJqW3btk393e9+18rNWnywCEC9kDBmTncn97dl/ODl1Y0pKSnR3Xff3fbDDz/8un379sUZGRnJQ4cOPdC9e/dKP7BUWxyhA4BLPv300/Pi4+NPdOnS5WTjxo3tkCFD9r/11lvnu1WPQAcAl2zbtq1hbGzsqW6KcXFxJ7dv397QrXoEOgC4pLLWKpV1YnQKgQ4ALmnbtu13jsjz8/Mbtm7duvh0j6kNAh0AXJKVlXVky5YtjdevX9/w+PHjZubMmZFDhw494FY9VrkAgEvCwsI0YcKEbwcMGNCptLRU119//d6qWvI6gfa5ADyJ9rkAgHMWgQ4AHkGgA4BHEOgA4BEEOgB4BIEOAB5BoAOAS4YNG5YQGRmZkZiYmFIX9fhgEYD6YWyEo+1zNfZgte1zR40atffOO+/cc8MNN7RztHYVOEIHAJcMHDjwcHR0dEld1SPQAcAjCHQA8AgCHQA8gkAHAI8g0AHAJdnZ2e169+6dtHnz5kYtW7ZMf/rpp6PcrMeyRQD1QxDLDJ327rvvbq7LehyhA4BHEOgA4BEEOgB4BIEOAB5BoAOARxDoAOARBDoAuGTjxo1hvXr16tS+ffuUjh07pjz66KMt3KzHOnQA9ULa1DRH2+euHrm62nXtYWFhmjBhQn7v3r2PFhYWhnTt2rXLoEGDDnXv3v24k3OpwBE6ALgkPj6+uHfv3kcl6YILLijr0KHDsW+//bahW/UIdACoA3l5eQ3Xrl3bJCsr67BbNQh0AHDZwYMHQ4YMGdJh/Pjx2yIjI8vcqkOgA4CLTpw4YQYPHtxh2LBh+0eOHHnAzVoEOgC4pKysTNdee218p06djo8dO3a32/UIdABwybx585rOmjWr+aJFi8KTkpK6JCUldXnjjTci3KrHskUA9UIwywyddvnllx+21tZZXY7QAcAjCHQA8AgCHQA8gkAHAI8g0AHAIwh0APAIli0CgEuOHj1qevXqlXTy5ElTWlpqsrOzC59++ukdbtUj0AHUC+uSkh1tn5u8fl2168sbN25sFy1alBcREVF24sQJc+GFF3b+5JNPDl522WVHnJxLBU65AIBLQkJCFBERUSZJJ0+eNCUlJcYY41491/YMAFBJSYmSkpK6tGzZMiMrK+tQ3759XTk6lwh0AHBVaGio1q9fv/bbb79dtWLFivOWLl3a2K1aBDoA1IGoqKjS3r17F7377ruuNeci0AHAJTt27Ajdu3dvA0k6fPiw+fTTT5slJye78vdEJVa5AIBrtm3bFvarX/2qXWlpqay15sorr9x/3XXXHXSrHoEOoF4IZpmh03r16nVs3bp1a+uqHqdcAMAjCHQA8AgCHQA8gkAHAI8g0AHAIwh0APAIAh0AXFZSUqLk5OQul156aUc367AOHUC98MLo+Y62z71tct+g17X/4Q9/aNmxY8djhw8fbuDkHAJxhA4ALtq0aVPYhx9+GHHjjTfudbsWgQ4ALrrtttvaPPXUU/khIe7HLYEOAC6ZPn16RFRUVMlPfvKTo3VRj3PoAOCSRYsWNZ03b975sbGxESdOnAg5cuRIyJVXXtnunXfe2exGPY7QAcAlL7zwwvbdu3ev2r59++q//e1v31x00UVFboW5RKADgGcYa+3ZngMAOC43N3dLRkaG6ytL3JSbmxuVkZGREOx4jtABwCMIdADwCAIdADyCQAcAjyDQAcAjCHQA8Ag+KQoALoqNjU0777zzSkNCQhQaGmrXrFmzzq1aBDqAemHCNVc42j733jfeC7p97mefffZ1TExMiZP1K8MpFwDwCAIdAFx22WWXJaakpCT/6U9/inKzDqdcAMBFX3zxxfqEhITi7du3h/bt27dTSkrK8YEDBx52oxZH6ADgooSEhGJJio2NLRk8ePCBL7/88jy3ahHoAOCSQ4cOhRQWFoZUXF+wYEGz9PT0Y27V45QLALgkPz8/NCcnp6MklZaWmqFDh+67+uqrD7lVj0AHUC/UZJmhU7p06XIyLy9vbV3V45QLAHgEgQ4AHkGgA4BHEOgA4BEEOgB4BIEOAB5BoAOAi/bu3dtgwIAB7du1a5fSvn37lI8//ti1T4qyDh1AvZA/ZqGj7XPjxv8kqHXtN910U5v+/fsf+uCDD745fvy4OXz4sGsH0gQ6ALhk//79If/617/C33rrrS2S1LhxY9u4ceNSt+pxygUAXLJ+/fpGkZGRJcOGDUtITk7ucs0118QfOnTItdwl0AHAJSUlJWbdunVNbrvttoJ169atbdKkSdlDDz3Uyq16BDoAuCQhIeFky5YtT/bt2/eIJF1zzTWFubm5TdyqR6ADgEvatm1b0qpVq5O5ubmNJOmjjz5q1rlz5+Nu1eOXogDgoueff/7bESNGtD958qRp27btienTp29xqxaBDqBeCHaZodMuueSSY2vWrFlXF7U45QIAHkGgA4BHEOgA4BEEOgB4BIEOAB5BoAOARxDoAOCS3NzcRklJSV0qLk2bNu06bty4Fm7VYx06gHph7NixjrbPHTt2bLXr2jMyMk6sX79+rSSVlJSoVatWGddee+0BJ+fhjyN0AKgDs2fPbta2bdsTnTp1OulWDQIdAOrA9OnTI6+++up9btYg0AHAZcePHzcff/xxxC9+8YtCN+sQ6ADgsrfeeiuiS5cuR9u0aVPiZh0CHQBc9vrrr0cOHz58v9t1CHQAcFFRUVHIokWLmv385z8/4HYtli0CqBeCWWbohvDw8LIDBw6srItaHKEDgEcQ6ADgEQQ6AHgEgQ4AHkGgA4BHEOgA4BEEOgC46JFHHmnRsWPHlMTExJTs7Ox2R48eNW7VYh06gHrhk/kdHG2fe1nfTdWua9+8eXPYSy+91DIvL29N06ZN7aBBg9r/5S9/ibzjjjtcadLFEToAuKi0tNQcOXIkpLi4WMeOHQuJi4srdqsWgQ4ALmnXrl3xbbfdtqtdu3bpLVq0yAgPDy8dMmTIIbfqEegA4JKCgoIGc+bMOX/jxo2rd+3atero0aMhf/7znyPdqkegA4BL3n333WZt27Y90bp165JGjRrZq6666sA///nPpm7VI9ABwCUJCQknV6xY0bSoqCikrKxM8+fPD09OTj7uVj1WuQCAS/r27XskOzu7MD09PTk0NFQpKSlH77nnngK36hlrrVv7BoCzJjc3d0tGRsbesz2P2sjNzY3KyMhICHY8p1wAwCMIdADwCAIdADyCQAcAjyDQAcAjCHQA8AgCHQBc9Oijj7ZITExM6dixY8q4ceNauFmLDxYBqBdaLVjpaPvcXZdmVts+d+nSpY1fffXV6BUrVqxr3LhxWVZWVqecnJyDaWlpJ5ycSwWO0AHAJatXr/5Rt27dDoeHh5eFhYXpxz/+cdEbb7xxvlv1CHQAcElmZuaxf/3rX+G7du1qUFRUFDJv3ryIbdu2NXSrHqdcAMAl3bp1O37nnXfu6tu3b6cmTZqUdenS5WhoqHuxyxE6ALjo7rvv3rt27dp1y5Yty4uMjCxNTEyk2yIAnIu2b98eGhsbW7Jhw4aGc+bMOX/JkiXr3apFoAOAi372s591OHDgQGhoaKh95plnvo2Oji51qxaBDqBeCGaZoRuWL1+eV1e1OIcOAB5BoAOARxDoAOARBDoAeASBDgAeQaADgEcQ6ADgkmHDhiVERkZmJCYmplRs2717d4NLLrkkMT4+PvWSSy5JLCgoaOBUPWOtdWpfAPCDkZubuyUjI2Nvxe2EMXMcbZ+7Zfzgate1v//++03Dw8PLbrjhhnYbNmz4tySNHj06LjIysuTxxx/f9bvf/a5VYWFhg0mTJm2v7PG5ublRGRkZCcHOiQ8WAYBLBg4ceDgvL+873RU/+OCD8z/77LM8Sbr55pv3ZWVldZZUaaDXFKdcAKAO7du3LzQ+Pr5YkuLj44v379/v2IE1gQ4AHkGgA0Adat68ecnWrVvDJGnr1q1hkZGRJU7tm0AHgDp0+eWXH3jxxRebS9KLL77YfMCAAQec2je/FAUAl2RnZ7dbvHhxeGFhYWjLli3Tx4wZs+ORRx7ZmZOT0yE+Pj6qdevWJ2fNmrXJqXosWwTgSYHLFs9FNV22yCkXAPAIAh0APIJABwCPINABwCMIdADwCAIdADyCQAcAl1TWPnfKlCkXdOzYMSUkJKT7559/3sTJenywCED9MDbC0fa5Gnuw2va5o0aN2nvnnXfuueGGG9pVbMvMzDw2Y8aMjTfeeGOCo/MRgQ4ArqmsfW63bt2Ou1WPUy4A4BEEOgB4BIEOAB5BoAOAR/BLUQBwSWXtc5s3b15y//33ty0sLAzNyclJTE5OPrpo0aINTtSjfS4AT6J9LgDgnEWgA4BHEOgA4BEEOgB4BIEOAB5BoAOARxDoAOCSytrnVvj973/f0hjTfefOnY59HogPFgGoF9KmpjnaPnf1yNVn1D5XkjZu3Bg2f/78ZjExMSednBNH6ADgkoEDBx6Ojo4uCdx+++23t/njH/+Yb4xxtB6BDgB16LXXXouIiYkpvvjii485vW9OuQBAHSkqKgp58sknYxYsWOBI75ZAHKEDQB1Zt25do/z8/Ebp6eldYmNj03bv3t2wW7duyd9++60jB9ccoQNAHenZs+ex/fv351bcjo2NTVu2bNm6mJiY751nPxMcoQOAS7Kzs9v17t07afPmzY1atmyZ/vTTT0e5WY8jdAD1QjDLDJ327rvvbj7d/du3b1/tZD2O0AHAIwh0APAIAh0APIJABwCPINABwCMIdADwCAIdAFxSWfvce+65p3WLFi3Sk5KSuiQlJXV54403Ipyqxzp0APXCuqRkR9vnJq9fd8btc0ePHr173Lhxu52cj8QROgC4pqr2uW4h0AGgjr3yyistOnXq1GXYsGEJBQUFDZzaL4EOAHXo7rvv3rN169bV69atW9uqVaviW2+9tY1T+ybQAaAOtWnTpiQ0NFQNGjTQ7bffXrBy5crznNo3gQ4AdWjr1q1hFddff/318zt37uzYXy5ilQsAuCQ7O7vd4sWLwwsLC0NbtmyZPmbMmB2fffZZ+Nq1a38kSXFxcSf/+te/bnWqnrHWOrUvAPjByM3N3ZKRkbH3bM+jNnJzc6MyMjISgh3PKRcA8AgCHQA8gkAHAI8g0AHAIwh0APAIAh0APIJ16ADgkmHDhiV88sknEc2bNy/ZsGHDvyVp8ODB7Tdt2tRYkoqKihqEh4eXrl+/fq0T9Qh0APXCC6PnO9o+97bJfc+ofe6cOXO+qbh+4403xkVERJQ6NScCHQBcMnDgwMN5eXkNK7uvrKxM7777buS8efPynKrHOXQAOAs+/PDDplFRUcVpaWknnNongQ4AZ8G0adMihw4dut/JfXLKBQDqWHFxsT744IMLlixZ4sgvQytwhA4Adeydd95p1r59++MdOnQodnK/BDoAuCQ7O7td7969kzZv3tyoZcuW6U8//XSUJE2fPj1y2LBhjp5ukWifC8CjaJ8LADhnEegA4BEEOgB4BIEOAB5BoAOARxDoAOARBDoAuGTYsGEJkZGRGYmJiSkV2/75z3/+KCMjIykpKalLampq8oIFC5o4VY+P/gOoFyZcc4Wj7XPvfeO9M2qfe//998c9+OCDO4YPH37ojTfeiPjtb3/bZsmSJY50XOQIHQBcMnDgwMPR0dEl/tuMMTp48GADSTpw4ECDli1bnnSqHkfoAFCHnnvuuW2DBw9OfOihh9qUlZVp0aJF653aN0foAFCHnnvuuegnnnhi265du1Y9/vjj2371q18lOLVvAh0A6tCMGTOa//KXvzwgSaNGjSpctWrVeU7tm0AHgDoUHR1dPHfu3HBJevfdd8Pj4+OPO7VvzqEDgEuys7PbLV68OLywsDC0ZcuW6WPGjNkxadKkrffcc0+be++91zRq1Khs8uTJW52qR/tcAJ5E+1wAwDmLQAcAjyDQAcAjCHQA8AgCHQA8gkAHAI8g0AHAJZW1z/3yyy9/lJmZmdSpU6cuffv27bh//37Hcph16AA8KXAdev6YhY62z40b/5Nq2+e+//77TcPDw8tuuOGGdhs2bPi3JKWmpiY/+eST2wYPHnz4mWeeab558+ZGzz777I7KHs86dAD4gaisfe6WLVsaDxw48LAkXXHFFYfee++9C5yqR6ADQB1KTEw89n//93/nS9K0adMid+3a1dCpfRPoAFCHpkyZsmXSpEnRKSkpyUVFRSFhYWGOnfemORcA1KGuXbse/+KLLzZI0qpVqxp99NFH5zu1b47QAaAObd++PVSSSktL9fDDD8f8+te/3uPUvjlCBwCXVNY+9/DhwyGvvPJKC0kaNGhQ4R133LHPqXosWwTgSbTPBQCcswh0APAIAh0APIJABwCPINABwCMIdADwCAIdAFyycePGsF69enVq3759SseOHVMeffTRFpK0e/fuBpdccklifHx86iWXXJJYUFDQwIl6fLAIQL0wduxYR9vnjh07ttr2uWFhYZowYUJ+7969jxYWFoZ07dq1y6BBgw69/PLLUX369Cl6/PHHN/zud79r9fvf/77VpEmTttd2TgQ6ALgkPj6+OD4+vliSLrjggrIOHToc+/bbbxt+8MEH53/22Wd5knTzzTfvy8rK6iyp1oHOKRcAqAN5eXkN165d2yQrK+vwvn37QiuCPj4+vnj//v2OHFwT6ADgsoMHD4YMGTKkw/jx47dFRkaWuVWHQAcAF504ccIMHjy4w7Bhw/aPHDnygCQ1b968ZOvWrWGStHXr1rDIyMiS0+4kSAQ6ALikrKxM1157bXynTp2Ojx07dnfF9ssvv/zAiy++2FySXnzxxeYDBgw44EQ9fikKAC6ZN29e01mzZjVPTEw8lpSU1EWSHnnkke2PPPLIzpycnA7x8fFRrVu3Pjlr1qxNTtSjfS4AT6J9LgDgnEWgA4BHEOgA4BEEOgB4BIEOAB5BoAOARxDoAOCSqtrnTpky5YKOHTumhISEdP/888+bOFWPDxYBqBc+md/B0fa5l/XddMbtczMzM4/NmDFj44033pjg5JwIdABwSVXtc3Nycg65UY9TLgBQB/zb57pVg0AHAJfRPhcAPKCy9rluIdABwCVVtc91C78UBQCXVNU+98SJE+b+++9vW1hYGJqTk5OYnJx8dNGiRRtqW4/2uQA8ifa5AIBzFoEOAB5BoAOAR5y1X4pGRUXZhISEs1UegMc99dRTWrt2bfzZnkdt7Nu3Tz169PjOLzqXL1++11obXdn4sxboCQkJWrZs2dkqD8Dj1q1bp+Tk5LM9jVoxxnwvJ40xW6sazykXAPAIAh0AXLJt2zZdeumlSk5OVkpKip599llJ0v3336+kpCSlp6crJydHBw4ccKQeHywCUC+0WrDS0f3tujSz2jGhoaGaMGGCunXrpqKiInXv3l39+vVTv3799MQTTyg0NFS//e1v9cQTT+jJJ5+s9Zw4QgcAl8TExKhbt26SpPDwcCUnJ2v79u3q37+/QkPLj6cvuugi5efnO1Kv2kA3xjQ2xiwxxuQaY/5tjHmkkjHGGPOcMWajMWaVMaabI7MDAI/YsmWLvvrqK/Xq1es726dMmaKBAwc6UiOYUy4nJPW11h42xoRJWmSMed9au9hvzEBJib5LL0mTfF8BoN47fPiwhg4dqmeeeUbNmjU7tf2xxx5TaGioRowY4UidagPdljd7qWjIHua7BDaAuVLSq76xi40x5xtjYqy1Ox2ZJQCco4qLizV06FCNGDFCQ4YMObV96tSpeu+99/TJJ5/IGONIraDOoRtjGhhjVkraI2metfZfAUNiJW3zu53v2wYA9Za1Vr/+9a+VnJyse+6559T2Dz74QE8++aRmz56tJk0c+xvRwQW6tbbUWpspKU5ST2NMasCQyv57+V4bR2PMTcaYZcaYZQUFBTWeLACcS7744gv9/e9/1/z585WZmanMzEzNnTtXt99+u4qKitSvXz9lZmZq9OjRjtSr0bJFa+0BY8ynkgZIWuN3V76kNn634yTtqOTxL0l6SdL3Ps4KAG4KZpmh03r37q3KWpQPGjTIlXrBrHKJNsac77v+I0k/lbQ+YNhsSb/0rXa5SNJBzp8DQN0K5gg9RtJUY0wDlf8H8A9r7XvGmNGSZK2dLGmupEGSNko6KukGl+YLAKhCMKtcVknqWsn2yX7XraTbnJ0aAKAm+KQoAHgEgQ4AHkGgA4BHEOgA4JKq2uc+9NBDSk9PV2Zmpvr3768dO763yvuMmMrWSNaFHj16WP5iEQC3BP7FooQxcxzd/5bxg6sds3PnTu3cufM77XNnzZqluLi4Uz1dnnvuOa1du1aTJ0/+3uMr+6tLxpjl1toeldXjCB0AXFJV+1z/Bl1HjhxxrJcLf+ACAOpAYPvcBx98UK+++qoiIiK0YMECR2pwhA4ALqusfe5jjz2mbdu2acSIEZo4caIjdQh0AHBRVe1zK1x//fWaMWOGI7UIdABwSVXtczds2HDq+uzZs5WUlORIPc6hA4BLKtrnpqWlKTMzU5L0+OOP65VXXlFeXp5CQkIUHx9f6QqXM0GgA6gXgllm6LQfXPtcAMC5gUAHAI8g0AHAIwh0APAIAh0APIJABwCPINABwCVVtc+t8Kc//UnGGO3du9eReqxDB1A/jI1weH8Hqx0SGhqqCRMmfKd9br9+/dSlSxdt27ZN8+bNU9u2bR2bEkfoAOCSqtrnStLdd9+tp556yrHWuRKBDgB1wr997uzZsxUbG6uMjAxHa3DKBQBc5t8+NzQ0VI899pg++ugjx+twhA4ALgpsn7tp0yZt3rxZGRkZSkhIUH5+vrp166Zdu3bVuhZH6ADgksra56alpWnPnj2nxiQkJGjZsmWKioqqdT2O0AHAJRXtc+fPn6/MzExlZmZq7ty5rtWr9gjdGNNG0quSWkkqk/SStfbZgDF9JL0jabNv00xr7ThHZwoAtRHEMkOnVdU+19+WLVscqxfMKZcSSfdaa1cYY8IlLTfGzLPWrg0Yt9Bae4VjMwMA1Ei1p1ystTuttSt814skrZMU6/bEAAA1U6Nz6MaYBEldJf2rkrsvNsbkGmPeN8akVPH4m4wxy4wxywoKCmo+WwBAlYIOdGNMU0kzJN1lrT0UcPcKSfHW2gxJz0uaVdk+rLUvWWt7WGt7REdHn+GUAQCVCSrQjTFhKg/z16y1MwPvt9YestYe9l2fKynMGFP7NTgAgKBVG+imvNHAK5LWWWv/t4oxrXzjZIzp6dvvPicnCgA4vWCO0H8s6ReS+hpjVvoug4wxo40xo31jrpa0xhiTK+k5Sdfa6tbqAIDHVdU+d+zYsYqNjXV8bXq1yxattYsknbYdmLV2oqSJjswIAFyQNjXN0f2tHrm62jFVtc+Vyrst3nfffY7OiY/+A4BLYmJiFBMTI+n77XPdwEf/AaAO+LfPlaSJEycqPT1do0aNUmFhoSM1CHQAcJl/+9xmzZrplltu0aZNm7Ry5UrFxMTo3nvvdaQOgQ4ALgpsnytJLVu2VIMGDRQSEqIbb7xRS5YscaQWgQ4ALqmsfa4k7dy589T1t99+W6mpqY7U45eiAOCSiva5aWlpyszMlCQ9/vjjmj59ulauXCljjBISEvTiiy86Uo9AB1AvBLPM0GlVtc8dNGiQK/U45QIAHkGgA4BHEOgA4BEEOgB4BIEOAB5BoAOARxDoAOCSqtrnStLzzz+vzp07KyUlRQ888IAj9ViHDqBeWJeU7Oj+ktevq3ZMVe1zd+/erXfeeUerVq1So0aNtGfPHkfmRKADgEuqap/78ssva8yYMWrUqJEkqUWLFo7U45QLANQB//a5X3/9tRYuXKhevXopKytLS5cudaQGR+gA4LLA9rklJSUqLCzU4sWLtXTpUg0fPlzffPONfH+a+YxxhA4ALqqsfW5cXJyGDBkiY4x69uypkJAQ7d27t9a1CHQAcElV7XOvuuoqzZ8/X5L09ddf6+TJk4qKiqp1PU65AIBLqmqfO2rUKI0aNUqpqalq2LChpk6dWuvTLRKBDqCeCGaZodOqap8rSdOmTXO8HqdcAMAjCHQA8AgCHQA8otpAN8a0McYsMMasM8b82xhzZyVjjDHmOWPMRmPMKmNMN3emCwCoSjC/FC2RdK+1doUxJlzScmPMPGvtWr8xAyUl+i69JE3yfQUA1JFqj9CttTuttSt814skrZMUGzDsSkmv2nKLJZ1vjIlxfLYAgCrV6By6MSZBUldJ/wq4K1bSNr/b+fp+6ANAvVJV+9xrrrlGmZmZyszMVEJCwqk16rUV9Dp0Y0xTSTMk3WWtPRR4dyUP+d7iS2PMTZJukqS2bdvWYJrwghdGz9dtk/ue7WmgFs7lf8MXRs93dH/BvA5Vtc994403To259957FRER4cicgjpCN8aEqTzMX7PWzqxkSL6kNn634yTtCBxkrX3JWtvDWtsjOjr6TOYLAOeMmJgYdetWvkbEv31uBWut/vGPf+i6665zpF4wq1yMpFckrbPW/m8Vw2ZL+qVvtctFkg5aa3c6MkMA8AD/9rkVFi5cqJYtWyoxMdGRGsGccvmxpF9IWm2MWenb9jtJbSXJWjtZ0lxJgyRtlHRU0g2OzA4APCCwfW6F6dOnO3Z0LgUR6NbaRar8HLn/GCvpNqcmBQBeUVn7XEkqKSnRzJkztXz5csdq8UlRAHBJVe1zJenjjz9WUlKS4uLiHKtHoAOASyra586fP//UMsW5c+dKkl5//XVHT7dItM8FUE+cjeWWp2uf+7e//c3xehyhA4BHEOgA4BEEOgB4BIEOAB5BoAOARxDoAOARBDoAuOT48ePq2bOnMjIylJKSoocffliStH//fvXr10+JiYnq16+fCgsLHanHOnQA9cKEa65wdH/3vvFetWMaNWqk+fPnq2nTpiouLlbv3r01cOBAzZw5U5dddpnGjBmj8ePHa/z48XryySdrPSeO0AHAJcYYNW3aVFJ5T5fi4mIZY/TOO+9o5MiRkqSRI0dq1qxZjtQj0AHARaWlpcrMzFSLFi3Ur18/9erVS7t371ZMTPlf6YyJidGePXscqUWgA4CLGjRooJUrVyo/P19LlizRmjVrXKtFoANAHTj//PPVp08fffDBB2rZsqV27iz/G0A7d+5UixYtHKlBoAOASwoKCnTgwAFJ0rFjx061zP3Zz36mqVOnSpKmTp2qK6+80pF6rHIBAJfs3LlTI0eOVGlpqcrKyjR8+HBdccUVuvjiizV8+HC98soratu2rd58801H6hHoAOqFYJYZOi09PV1fffXV97Y3b95cn3zyieP1OOUCAB5BoAOARxDoAOARBDoAeASBDgAeQaADgEcQ6ADgkqra57755ptKSUlRSEiIli1b5lg91qEDqBfyxyx0dH9x439S7Ziq2uempqZq5syZuvnmmx2dU7VH6MaYKcaYPcaYSjvKGGP6GGMOGmNW+i6/d3SGAHCOqqp9bnJysjp37ux4vWBOufxN0oBqxiy01mb6LuNqPy0A8IbK2ue6pdpAt9Z+Lmm/azMAAA87F9vnXmyMyTXGvG+MSXFonwDgGf7tc93iRKCvkBRvrc2Q9LykWVUNNMbcZIxZZoxZVlBQ4EBpAPjhqqp9rltqHejW2kPW2sO+63MlhRljoqoY+5K1toe1tkd0dHRtSwPAD9rOnTt16aWXKj09XRdeeKH69eunK664Qm+//bbi4uL05ZdfavDgwbr88ssdqVfrZYvGmFaSdltrrTGmp8r/k9hX65kBgIOCWWbotKra5+bk5CgnJ8fxetUGujFmuqQ+kqKMMfmSHpYUJknW2smSrpZ0izGmRNIxSddaa63jMwUAnFa1gW6tva6a+ydKmujYjAAAZ4SP/gOARxDoAOARBDoAeASBDgAeQaADgEuqap/70EMPKT09XZmZmerfv7927NjhSD3a5wKoF8aOHVvn+6uqfe7999+vRx99VJL03HPPady4cZo8eXKt58QROgC4pKr2uc2aNTs15siRIzLGOFKPI3QAcFFpaam6d++ujRs36rbbbjvVPvfBBx/Uq6++qoiICC1YsMCRWhyhA4CLqmqf+9hjj2nbtm0aMWKEJk505rOZBDoA1IGq2udef/31mjFjhiM1CHQAcElV7XM3bNhwaszs2bMda6nLOXQAcMnOnTs1cuRIlZaWqqysTMOHD9cVV1yhoUOHKi8vTyEhIYqPj3dkhYtEoAOoJ5xethiMqtrnOnWKJRCnXADAIwh0APAIAh0APIJABwCPINABwCMIdADwCAIdAFxSVftcSXr++efVuXNnpaSk6IEHHnCkHuvQAdQLn8zv4Oj+Luu7qdoxVbXPPXbsmN555x2tWrVKjRo10p49exyZE0foAOCSqtrnTpo0SWPGjFGjRo0kSS1atHCkHoEOAC4qLS1VZmamWrRooX79+qlXr176+uuvtXDhQvXq1UtZWVlaunSpI7U45QIALqpon3vgwAHl5ORozZo1KikpUWFhoRYvXqylS5dq+PDh+uabb2r9hy44QgeAOuDfPjcuLk5DhgyRMUY9e/ZUSEiI9u7dW+sa1Qa6MWaKMWaPMWZNFfcbY8xzxpiNxphVxphutZ4VAHhAVe1zr7rqKs2fP1+S9PXXX+vkyZOKioqqdb1gTrn8TdJESa9Wcf9ASYm+Sy9Jk3xfAaBeq6p97smTJzVq1CilpqaqYcOGmjp1qiN/V7TaQLfWfm6MSTjNkCslvWqttZIWG2PON8bEWGt31np2AOCQYJYZOq2q9rkNGzbUtGnTHK/nxDn0WEnb/G7n+7YBAOqQE4Fe2c8JttKBxtxkjFlmjFlWUFDgQOmaSxgz56zU/aHJH7PwbE/BVZ/M76AJ11zh6P6qc66+pmlT0872FM5Y/piFWpeUfLan4b6xEUENcyLQ8yW18bsdJ2lHZQOttS9Za3tYa3tER0c7UBoAUMGJQJ8t6Ze+1S4XSTrI+XMAqHvV/lLUGDNdUh9JUcaYfEkPSwqTJGvtZElzJQ2StFHSUUk3uDVZAEDVglnlcl0191tJtzk2IwDAGeGTogDgstLSUnXt2lVXXFH+i/qHHnpI6enpyszMVP/+/bVjR6W/dqwxerkAqBdaLVjp6P52XZoZ9Nhnn31WycnJOnTokCTp/vvv16OPPipJeu655zRu3DhNnjy51nPiCB0AXJSfn685c+boN7/5zaltzZo1O3X9yJEjjnxKVOIIHQBcddddd+mpp55SUVHRd7Y/+OCDevXVVxUREaEFCxY4UosjdABwyXvvvacWLVqoe/fu37vvscce07Zt2zRixAhNnDjRkXoEOgC45IsvvtDs2bOVkJCga6+9VvPnz9fPf/7z74y5/vrrNWPGDEfqEegA4JInnnhC+fn52rJli15//XX17dtX06ZN04YNG06NmT17tpKSkhypxzl0AKhjY8aMUV5enkJCQhQfH+/ICheJQAdQT9RkmaEb+vTpoz59+kiSY6dYAnHKBQA8gkAHAI8g0AHAIwh0APAIAh0APIJABwCPINABwGWB7XPHjh2r2NhYZWZmKjMzU3PnznWkDuvQAdQLTv+B+C3jBwc9NrB9riTdfffduu+++xydE0foAOCiytrnuoVABwAXVbTPDQn5btxOnDhR6enpGjVqlAoLCx2pRaADgEuqap97yy23aNOmTVq5cqViYmJ07733OlKPc+gA4JKK9rlz587V8ePHdejQIf385z/XtGnTTo258cYbT/2ytLY4QgcAl1TVPnfnzp2nxrz99ttKTU11pB5H6ABQxx544AGtXLlSxhglJCToxRdfdGS/BDqAeqEmywzd4N8+9+9//7srNTjlAgAeQaADgEcEFejGmAHGmDxjzEZjzJhK7u9jjDlojFnpu/ze+akCAE6n2nPoxpgGkl6Q1E9SvqSlxpjZ1tq1AUMXWmudWXsDAKixYI7Qe0raaK39xlp7UtLrkq50d1oAgJoKJtBjJW3zu53v2xboYmNMrjHmfWNMiiOzAwAELZhAN5VsswG3V0iKt9ZmSHpe0qxKd2TMTcaYZcaYZQUFBTWaKACcqwLb5+bm5uriiy9WWlqasrOzv9OFsTaCWYeeL6mN3+04STv8B1hrD/ldn2uM+bMxJspauzdg3EuSXpKkHj16BP6nAADuGRvh8P4OBj00sH3ub37zG/3pT39SVlaWpkyZoj/+8Y969NFHaz2lYI7Ql0pKNMa0M8Y0lHStpNn+A4wxrYwxxne9p2+/+2o9OwA4x1XWPjcvL0//9V//JUnq16+fZsyY4UitagPdWlsi6XZJH0paJ+kf1tp/G2NGG2NG+4ZdLWmNMSZX0nOSrrXWcgQOoN6rrH1uamqqZs8uPy5+8803tW3btqoeXiNBrUO31s611nay1naw1j7m2zbZWjvZd32itTbFWpthrb3IWvtPR2YHAOewqtrnTpkyRS+88IK6d++uoqIiNWzY0JF69HIBAJecrn3uRx99JEn6+uuvNWeOM38ej4/+A4BLqmqfu2fPHklSWVmZ/vCHP2j06NHV7Ck4BDoA1LHp06erU6dOSkpKUuvWrXXDDTc4sl9OuQCoH2qwzNAN/u1z77zzTt15552O1+AIHQA8gkAHAI8g0AHAIwh0APAIAh0APIJABwCPINABwEUJCQlKS0tTZmamevToIam8f0tKSopCQkK0bNkyx2qxDh1AvZA2Nc3R/a0euTrosQsWLFBUVNSp26mpqZo5c6ZuvvlmR+dEoANAHUtOTnZlv5xyAQAXGWPUv39/de/eXS+99JKrtThCBwAXffHFF2rdurX27Nmjfv36KSkp6dQft3AaR+gA4KLWrVtLklq0aKGcnBwtWbLEtVoEOgC45MiRIyoqKjp1/aOPPlJqaqpr9Qh0AHDJ7t271bt3b2VkZKhnz54aPHiwBgwYoLfffltxcXH68ssvNXjwYF1++eWO1OMcOoB6oSbLDJ3Svn175ebmfm97Tk6OcnJyHK/HEToAeASBDgAeQaADgEcQ6AA8y1p7tqdwxs5k7gQ6AE9q3Lix9u3bd06GurVW+/btU+PGjWv0OFa5APCkuLg45efnq6Cg4GxP5Yw0btxYcXFxNXpMUIFujBkg6VlJDST9xVo7PuB+47t/kKSjkn5lrV1Ro5kAgIPCwsLUrl27sz2NOlXtKRdjTANJL0gaKKmLpOuMMV0Chg2UlOi73CRpksPzBABUI5hz6D0lbbTWfmOtPSnpdUlXBoy5UtKrttxiSecbY2IcnisA4DSCCfRYSdv8buf7ttV0DADARaa63wAbY4ZJutxa+xvf7V9I6mmt/W+/MXMkPWGtXeS7/YmkB6y1ywP2dZPKT8lIUmdJeQHloiTtrWbOTo2hnvfn5PV6P8Q5eb3eD2FO8dba6EpHW2tPe5F0saQP/W7/j6T/CRjzoqTr/G7nSYqpbt+V1FpWV2Oo5/05eb3eD3FOXq/3Q5yT/yWYUy5LJSUaY9oZYxpKulbS7IAxsyX90pS7SNJBa+3OIPYNAHBItcsWrbUlxpjbJX2o8mWLU6y1/zbGjPbdP1nSXJUvWdyo8mWLN7g3ZQBAZYJah26tnavy0PbfNtnvupV0mwPzCeYP7jk1hnp1P4Z6dT+GenU/5mzUkxTEL0UBAOcGerkAgEcQ6ADgEQQ6AHjEDz7QjTFJxpjLjDFNA7YP8Lve0xhzoe96F2PMPcaYQdXs99Ugavf27au/37Y7jDFtqnlcQ2PML40xP/Xdvt4YM9EYc5sxJixgbAdjzH3GmGeNMROMMaONMRHVzQ3nLmNMC4f209yJ/ZzLvP4a1Pj51WTRel1dJN3g+3qHyj+kNEvSFklX+o1Z4fv6sKTFkpZJekLSfEm/l/S5pAd9Y2YHXN6VdLjitt8+l/hdv1HSSt/+v5A0xrf9oKQdkhZKulVSdCXzf03SG746f5f0tqRfSPqbpKl+4+6QNE/S/5P0T0l/lvSYpLWS+pztf4cz+HdrcRZrR0gaL2m9pH2+yzrftvOD3Mf7vq/NfO+lv0u6PmDMn31fW6m8Cd0LkppLGitptaR/yO9DdZIiAy7Nfe/lCyRF+sYMCHger0haJen/JLX0bR8vKcp3vYekb1S+THirpKyK7wnfe6lDNc+zh6QFkqZJauN7Dx5U+WdOuvrGNJU0TtK/ffcV+L7PflXT1zyY18qp16Cun18w867B+y6o53fafZ2tb8BqnuC3vq+rJTX1XU9QeWjf6bv9ld+YBpKaSDokqZlv+48krfJ7o0+T1EdSlu/rTt91/zfCV37Xl8oX1pLOk7S6YozKf7Lp7/vHK5D0gaSRksJ9YyrqhkraLamB77apuM9/7r7rTSR96rve1u/5nctBVW3AyLlvvg8l/VZSq4Ag+a2keX7bulVx6S5pp2/MDN/re5XK/9OfIalRxXPyff1A0n9LGqPyb+Df+v7d/lvSO371yiRtDrgU+75+479P3/W/SPqDpHhJd0uaVfFe8RuzQNKFvuud5Ps0oW+ff5L0raQlvse3ruQ1X6LyDqnXqbwH09W+7ZdJ+tJ3/R1Jv5IUJ+keSQ+pvJvqVEmP1/A1r/a1cuo1qOvnF8y8a/C+C+r5nfZ73YkAPpOL7x+2sstqSSd8Y9YGPKap783xv5JW+rZ95Xf/VwHjK8aE+F7geZIyfdu+qWROuSoPpOaBL6D+E7ArAraHSfqZpOmSCnzb1khq6NtXkf4TcI0lrfN77Gr9JygukLTc7741HgiqagNGzn3z5Z3mvZbnd71U5T/FLajkcsz/feP3mAdV/lNac7/Xyf99921l7zvf9ft8r2ma37bNAeNXVPbYgPfwekmhvuuLA8asrmQ/P1H5T3y7fM/tpsq+TyqZe8X7PDdg+1K/76X1NXzNq32tnHoN6vr5BTPvGrzvgnp+p7uczUDfLSlT5f+b+V8SJO3wjZkvXwD7PS5U0quSSn23/yWpScU/ht+4CH0/fOMkvSlpYuA/tO/+LSr/MWez72sr3/amquQ/kEoe/yPf17t9j9+q8tMqn0h6WeUB/rDf+DtVHpov+f4xK041RUv6vIbfND/0oKo0YKqp95UN/pvvI0kPyO/HXEktVf4f0sd+29ZISqzi9dzm+7rO/73k2zZS5T8hbA2ck6Q/BIxdHXC74n33v5LCFXAwofLupPdIutf3vjF+91X8tPffvufYV+U/NT0j6b8kPSLp74Gvt9/jG0gaIOmvftu+VPlPmMNU/h69yrc9S/852v+npN6+69n6bj+nijAL9jU/3Wu1ysnXoK6fXzDzrsH7Lqjnd7rL2Qz0Vype0Eru+z+/b4RWVYz5se9royruj5Jf2ATcN1i+I7sg59pEUjvf9U5BPqa1fEejks6XdLXKu1QGjkvx3ZdUxX7O5aCqNmAc/Oa7QNKTKv+PsVDSft/zfVK+n5B8466W1LmK16mi9lOSflrJ/QMkbfBdHyff6cCAMR0lvVXF/rNVfqpoV8D2hwMuFaf6Wqn87wxUjOuj8t/NfKXyg4O5Ku9eGua7//Ug35sZKv/J731JSSr/a2MHfO+DS/zGLPFtX1Txmqn8YOOOGr7m1b5WTr0Gp3l+hb7n9+Mqnl+nIJ5foe/5PaX//NQd7Lyrfd8F+/xO+28bzCAuZ+8S8KbaH/BNc0FN3jCq+6CqNmCq+OY7oO+GS3p133y+20mSfho4f/n94spv3GWnG3eaMQNrsp/AcSr/3U5qDeo5PsZ3OzmIfSVX93qq/A/gVJzrTVH5keqgSv6d/cd1UflR7aBajjldvV7VjQsYU2m9SvZb7ZGy/IL8NGN6++r1P82Yn/jmXeWY7z0m2IFcfngX+U7RODGutmMCgsr1eoFjFMSKqGDHqfxH31qPcbieI/vx29f6IOpVN+ZhfXeF2ScKWGFWxbjKVqKdyZhg631vXJD1AlfHzVbA6rhgxvjGBbOCzn/Mb1R+lP6dMdV+PwQziMsP86JKfg9wpuOcGlPX9VSDFVHBjnNqTF3XO0tzOu0Ks2DHOTXG4XrVro5Teeg6toKuujHVXYLqtoizxxizqqq7VH4uPehxTo2p63pBzqmBtfawJFlrtxhj+kh6yxgT7xunGoxzakxd16vrOZVYa0slHTXGbLLWHvKNP2aMKfOrF8w4p8Y4ua8eKl+48KCk+621K40xx6y1n/nV6h7EGEkKMcZcoPJf5BtrbYGv3hFjTEkNxpxeMKnP5exdFMRqoGDHOTWmrusFOabaFVHBjnNqTF3XOwtzCmqFWTDjnBrj9L582067Oi6YMQpuBV21Y6rNi7oKJi5ndlEQq4GCHefUmLquF+SYaldEBTvOqTF1Xe8szCmoFWbBjHNqjNP7Criv2tVxwYwJGH9qBV1txlRc6IcOAB4RcrYnAABwBoEOAB5BoAM+xpgtxpgop8YBdY1ABwCPINBR7xhjEowx640xU40xq4wxbxljmvju/m9jzApjzGpjTJJvfHNjzEfGmK+MMS/qu2u6gR8MAh31VWdJL1lr01X+ScFbfdv3Wmu7qbwn/H2+bQ9LWmSt7aryj3S3revJAsEg0FFfbbPWfuG7Pk3lzZIkaabv63KVf3BJKm9hOk2SrLVzVN51D/jBIdBRXwV+AKPi9gnf11LpO60x+MAGfvAIdNRXbY0xF/uuX6fytrxV+VzSCEkyxgxUeUtj4AeHQEd9tU7SSF/jr0iVnzOvyiOS/ssYs0Llf4zj2zqYH1BjfPQf9Y4xJkHSe9ba1LM9F8BJHKEDgEdwhA4AHsEROgB4BIEOAB5BoAOARxDoAOARBDoAeASBDgAe8f8BdDyV2P2DQ+cAAAAASUVORK5CYII=\n",
      "text/plain": [
       "<Figure size 432x288 with 1 Axes>"
      ]
     },
     "metadata": {
      "needs_background": "light"
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "pd.crosstab(df.phd,df.service).plot(kind=\"bar\")"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 29,
   "id": "76b269aa",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "Prof         46\n",
       "AsstProf     19\n",
       "AssocProf    13\n",
       "Name: rank, dtype: int64"
      ]
     },
     "execution_count": 29,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df[\"rank\"].value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 31,
   "id": "156e37c1",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "<AxesSubplot:ylabel='sex'>"
      ]
     },
     "execution_count": 31,
     "metadata": {},
     "output_type": "execute_result"
    },
    {
     "data": {
      "image/png": "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\n",
      "text/plain": [
       "<Figure size 432x288 with 1 Axes>"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "df.sex.value_counts().plot(kind=\"pie\")"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 32,
   "id": "1afd1862",
   "metadata": {},
   "outputs": [],
   "source": [
    "import seaborn as sns"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 33,
   "id": "5ca90235",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "<AxesSubplot:xlabel='sex', ylabel='service'>"
      ]
     },
     "execution_count": 33,
     "metadata": {},
     "output_type": "execute_result"
    },
    {
     "data": {
      "image/png": "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\n",
      "text/plain": [
       "<Figure size 432x288 with 1 Axes>"
      ]
     },
     "metadata": {
      "needs_background": "light"
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "sns.boxplot(x=\"sex\",y=\"service\",data=df)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 34,
   "id": "6191b710",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "<seaborn.axisgrid.PairGrid at 0x1c728f22ca0>"
      ]
     },
     "execution_count": 34,
     "metadata": {},
     "output_type": "execute_result"
    },
    {
     "data": {
      "image/png": "iVBORw0KGgoAAAANSUhEUgAAAWUAAAFlCAYAAAAzhfm7AAAAOXRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjMuNCwgaHR0cHM6Ly9tYXRwbG90bGliLm9yZy8QVMy6AAAACXBIWXMAAAsTAAALEwEAmpwYAAA0zElEQVR4nO3dfXzU9Z3v/dcnBAy3MUAIKSRgaqwKGrVpa1tprbgua22lWrXtVcueQw8+zrYLPd1zra5H26utp0ev0/WqrvvYI9Vuqd12Ydcqroe1slirrq0VvAPUI0oBwRBClECQAGE+1x/zm3GSzCQzmfnN7fv5eMxjZn538/3Rn59+8735fM3dERGR4lBV6AKIiMh7FJRFRIqIgrKISBFRUBYRKSIKyiIiRURBWUSkiJREUF60aJEDeumV69eI9OzpFdIrpZIIyvv37y90EaRC6dmTfCuJoCwiUikUlEVEikh1oQsgIlKqIhFnR/dhOg/20TClhrnTJlJVZVldU0FZRGQUIhHnka17+eaaF+g7HqFmbBW3X30Oi+bNzCowq/lCRGQUdnQfjgdkgL7jEb655gV2dB/O6roKyiIio9B5sC8ekGP6jkfYd6gvq+sqKIuIjELDlBpqxg4MoTVjq5gxuSar6yooi4iMwtxpE7n96nPigTnWpjx32sSsrquOPhGRUaiqMhbNm8npyxew71AfMyZr9IWISEFVVRkt9ZNoqZ+Uu2vm7EoiIpI1BWURkSKioCwiUkQUlEVEiog6+kREcijbfBgKyiIiOZKLfBihNl+Y2Q4z22xmL5jZxmDbVDNbb2bbgve6MMsgIpIvuciHkY825U+5+znu3h58vwHY4O6twIbgu4hIyctFPoxCdPRdDqwKPq8CFhegDCIiOZeLfBhhB2UHHjWzTWa2LNjW4O4dAMH7jJDLICKSF7nIhxF2R9/H3f0tM5sBrDezV9M9MQjiywCam5vDKp/IEHr2ZLRykQ8j1Jqyu78VvO8DHgA+DHSaWSNA8L4vxbkr3b3d3dvr6+vDLKbIAHr2JBuxfBjnt0ynpX5SxgmKQgvKZjbRzCbHPgOXAFuAh4AlwWFLgLVhlUFEpNSE2XzRADxgZrHf+bm7P2JmzwJrzGwpsAu4KsQyiIiUlNCCsrtvB9qSbO8GFob1uyIipUy5L0REioiCsohIEVFQFhEpIgrKIiJFRFniRKRiJUuzCWSVejNbCsoiUpGSpdm860vncqzfs0q9mS01X4hIRUqWZvOl3T1Zp97MloKyiFSkZGk2I07WqTezpaAsIhUpWZrNMUbWqTezpaAsIhUpWZrNs2bXZp16M1vq6BORipQqzSaQVerNbCkoi0jFiqXZbKmfNGB7sm15K1NBflVERJJSUBYRKSIKyiIiRURBWUSkiIQelM1sjJk9b2YPB9+nmtl6M9sWvNeFXQYRkVKRj5ryCuCVhO83ABvcvRXYEHwXkQoUiTjbu3r57Rv72d7VSyTihS5SwYUalM1sNvBp4J6EzZcDq4LPq4DFYZYhX2Y1NWNmWb1mNWk5e6kcsYRAl975JF/80TNceueTPLJ1b8UH5rDHKf8Q+EtgcsK2BnfvAHD3DjObEXIZ8uKt3W9yzd1PZ3WN1dd9LEelESl+yRICfXPNC5y+fEHBxggXg9CCspldBuxz901mduEozl8GLANoblYNUvJHz15+JEsI1Hc8wtuHj8b3J8tnnCwHcj5n3IUtzJryx4HPmtmlQA0wxcx+BnSaWWNQS24E9iU72d1XAisB2tvbK/vvGckrPXv5EUsIlBiY50wbz54DfXz53t8nzWecLAdyvvMdhy20NmV3/yt3n+3uc4EvAI+5+5eBh4AlwWFLgLVhlUFEUit0J1uyhEDfu/wsrr//pZT5jFM1eeQz33HYCpH74lZgjZktBXYBVxWgDCIVrRhqnMkSAqVq0th3qI+W+kkj7i8HeQnK7v448HjwuRtYmI/fFZHkiqWTLVlCoMFNGon5jJM1eeQ733HYNKNPpAINV+MspGRNGon5jEfaXw6UulOkAhVrjTNVjuNYk8pI+8uBgrJIBZo7bSJ3felcXtrdQ8SjyyCdNbt21DXOXA5TS5XjON39pU5BWaRCHet3Vj6xfUBH32gUQ6dhOVGbskgFyuXQskoYppZPJR+Uc5FzonpcTdbXECkluezoy+ZaycZKF3r8dKGVfPNFrnJOKG+FVJJcdvSN9lqpmj3GVRtf//nzFdsUUvI1ZRHJXC6Hlo32WqmaPV7a3VPRTSElX1MWkczlcmjZaK+VqtljcGtFuc3YG4mCskiFyuXQstFcK1Wzx+BYXgzjp/NJzRciklexjrzuw0e57cqzhzR7nD27tqxn7I1ENWURyZvBnXtzpo1n5bXtjB1j8UknAOvKeMbeSFRTLiZV1VpSSsra4M69nd1HWHbfRhqm1NBSP4mqKos3hZzfMj2+rZKoplxMIv0amidlrRJSb2ZLNWURyZtY516iSuvIG4mCsojkTSWk3sxWmAun1gBPACcFv/PP7v5tM5sKrAbmAjuAq939nbDKISLFoxJSb2Zr2KAcBNCU3P3tYXYfBS5y914zGws8ZWb/ClwBbHD3W83sBuAG4PoMyy0ieZTP1JyVbqSa8ibAAQOagXeCzycTXV/vlFQnursDvcHXscHLgcuBC4Ptq4guE6WgLFKklJozv4ZtU3b3U9y9BfgV8Bl3n+7u04DLgF+OdHEzG2NmLwD7gPXu/gzQ4O4dwfU7gBlZ3oOIhEipOfMr3Y6+D7n7utgXd/9X4JMjneTuJ9z9HGA28GEzm59uwcxsmZltNLONXV1d6Z4mkrVKefbSTZGZaWrO/v4IL775Do9s6eDFNw/Q3x9Jepwkl25H334zuwn4GdEmiC8D3en+iLsfMLPHgUVAp5k1unuHmTUSrUUnO2clsBKgvb29shKqSkFVwrOXSZNEJqk5+/sjPPjiHm56cEv8urcsns/itllUV2uwVzrSDcpfBL4NPBB8fyLYlpKZ1QPHg4A8HrgYuA14CFgC3Bq8rx1FuUVKXi47zzK9VqomidOXLxjSAZfJen5bO3riATl23Zse3ELrjEm0NdWN6t4qTVpBORhlsSLDazcCq8xsDNFmkjXu/rCZ/RZYY2ZLiXYWXpXhdUVKXi47z0ZzrUxn1qW7nl9HT/Lr7u3po60po9uqWGn9PWFmp5nZSjN71Mwei72GO8fdX3L3c939bHef7+7fDbZ3u/tCd28N3ocbVidSlgq9Rl4mM+syuX5j7fik151Zqxl76Uq3+eKfgP8F3AOcCK84IpUhlzkgRnOtTJokMrn+vMYp3LJ4/pA25XmNtRndUyVLNyj3u/vfhVoSkQpSDGvkpdskkcn1q6urWNw2i9YZk9jb08fM2hrmNdaqky8Dw/5LmdnUYFbfv5jZ18ysMbZtpNl+IpJaodfIy6RJYvD1YzmQOw/2JR1KV11dRVtTHX88v5G2pjoF5AxlMqMP4C8G7W/JeYlEKkCh18jLpEki8fpvHz7KngN9LLtvo2b3hWTYoOzupwAEQ9r+DLiAaJB+kmgbs4iMUiHXyMu0ySN2fYAv3/v7tIbSyeik+3fFKuAM4E7gb4LPq8IqlIiEK50mj2Qz/lLVsF/rPDTsrEBJX7odfR9w97aE7782sxfDKJCI5Me4amPZJ1qIOFRZ9HtMqrHPH2iYnLSGvXnPQb6x+gU1ZeRAujXl583s/NgXM/sI8O/hFElEspFOTosd3Yf5+s+f584Nr3PXY69z54bX+frPn4939KXqCBxTxZAa9vKLWvnlc7uVqChH0q0pfwT4ipntCr43A6+Y2WaiWTrPDqV0IpKRdGf3jdTRl2r/3oN98U6/1zoPsXnPQe773U46evqGXENGJ92gvCjUUohITqSb02Kkjr7h9id2+n1j9Qs5GWst70k398XOsAsiItnrPNhH3YRxXHHebCyoGN+/afeQ2muyGX1nNE6h+/BRAJrrJnD71ecMqHHfduXZ8f1zp02MdxYOrpVrvb3shLZGn4jkX2NtDV/56Bzu2LAtHihXLGxl5pShtdfBM/q++Uen8Z1/eZl33j3G7VefwyVnNLBu+QI6D/Zx/IRz89rN7Ow+MqBJROvt5Z6m2oiUkRMR4gEZos0Xd2zYxolBeeaTNXPcvv41rjhvNnUTxvHq3oM88Xo0wX9jbQ3L7tvIzu4j8WNjHXqxpozzW6bTUj9JATkHVFMWKSP7DiXvoOvq7eP9M95rvkjVkXdSdRXXnj+HOx97r6b9/c+dRd2EcfHOvNix6tALh2rKImUk3ZScqY6bO31iPCBDNPje+MBmrmqfPeI1JTcUlEXKSLrJiZIdd/NlZ+KRSNIa9GnBpJHhrim5EVrzhZk1AT8FZgIRYKW73xFkl1sNzAV2AFe7+zthlUOkkqSbnCjxuMSOvM+0zUo6FO6MmVNYpw69vAizTbkf+At3f87MJgObzGw98KfABne/1cxuAG4Arg+xHCJFL9v1+pKdn9jem7h/xuQaxlRFl25qmFLDjMk1fPpvnqTveIT7N+1m+UWtA9qUb7/6HE6ZPnHA+GQJT2hB2d07gI7g8yEzewWYBVwOXBgctgp4HAVlqWDZrtc30vnJ9q9Y2MpPf7uTd949xl9f1RavGXf09HHf73ay9IIWzpo1hdMaJqtWnGd5aVM2s7nAucAzQEMQsGOBe0Y+yiBSrLJdr2+k85Ptv2PDNq44bzZ9xyM4DOj06+jp496nttNYW6NhbgUQelA2s0nA/cA33P1gBuctM7ONZraxq6srvAKKDBL2s5eYMOjFNw+wo7s3ZR6KdAyXx2K4/bEZf7vfeZflF7UOSTJ0fPDgZsmLUMcpm9lYogH5H9z9l8HmTjNrdPcOM2sE9iU7191XAisB2tvblaRV8ibMZy9ZU8LNl53JnGnj45MzILMhZ6PNY+HBnR05doIHX9jD0gtaMAN3WL1xF4vmz8zBHUumQqspm5kB9wKvuPvtCbseApYEn5cAa8Mqg0ixSdaU8L2HX+b6RWcMGXLWXDdhxBScMPIwuMH7LzlzOn//px/itIZJ/PQ/foiPt07l+kVncO9T27nrsde596ntXL/oDA15K5Awa8ofB64FNpvZC8G2G4FbgTVmthTYBVwVYhlEikqqpoTX9/Wy9IIWzp41hdaGyTTXTeDRVzrT6vwbaRhc4v7DR4/zSkcv/+Enz8av+93L5/PZ+Y0a8lYkwhx98RTvLbg62MKwflekmKVqSjjaH+Hep7azLkixub2rN60UnDEjrdEX279xx9t866EtA677rbVbaJk+kfa5UzXkrQgo94VIjg035jhZusvlF7WyeuOuAU0Ow62FF7tOJjXZ/v4IWzt66Ojp44fXnEPHgSN0v3sciKb27DyYXqeihE9BWSSHRhozPHgm3YRxYzh+IsKi+TMHBNpUNerRrIXX3x/hwRf3cNODWwaMU75/027eefcYKxa2Muvk8aH9m0hmlPtCJIfSGXMca0r46Pun09ZUR/vcaUPGAyfrvBvtWnhbO3riATlWpsRxynds2MbEk1Q/Kxb6X0Ikh0Za+y5diTXqbNfC6+gZfpxy3/EI3YeP0srktMsn4VFQFsmhkcYMZyJXa+E11o4fdpyy0nAWFzVfiORQuqkz83nNeY1TuGXx/AHnr1gYbQpRGs7io5pyuamqxiy78aXvm93Enjd35ahAlSXd1Jn5vGZ1dRWL22bROmMSe3v6aKytYXLNWM5tPlljkouQgnK5ifRzzd1PZ3WJ1dd9LEeFqUwjjRmOySRdZ7rXTKW6uoq2pjramt7bdorGJBclBWWRAsg2XaeUL7UpixRAtuk6pXyppixSAOnM2AOyWo1ESpOCskgBjDRj764vncuxflfzRgVS84UMFYzgyOY1q6m50HcRmsQk9cOl1Bzu/CqD73/urKQz9uomjKPvWIRX9x7kqwtaaKytUfNGBVFNWYbSCI6UcrmeXt2EcSz7RAunzZjMK3sPcd/vdgJw7flz+K///OKAhEWx2XydBzObGSilRzVlkQzkcj29jp4+7tzwOhjc+9R2Onr6uOK82fGVpGPXv/OxaJ6KmrFVTBg3JrR7k+KgoCySgZHWw4PhmzeSnZ+4Rp4ZSa8/pgqWX9RK9+Gjo2oykdIR5nJQPzazfWa2JWHbVDNbb2bbgve6sH5fJAyxDrpEibkjYs0Tl975JF/80TNceueTPLJ1bzyIJjv/yLETrN64i6UXtPCBhslJr3/qjMms3riLTTt7hlxTykuYNeWfAIsGbbsB2ODurcCG4LtIyRgpD0Wq5o1dbx9me1cvnQf7+NG17cyZNj5+/lmza7n5sjMZUwV7DrzLty47c0gH4F8/+irXtDePKnWnlJYwl4N6wszmDtp8OXBh8HkV8DhwfVhlEMm1kfJQJGueqJswjud2HeDGBzbHO+9uu/JsZp1cw9SJJ8XX41v5xHb6jkeYM208K69tZ+wYY8K4MXQfPsplZ88adepOKS35blNucPcOgOB9Rp5/XyRrsTwU57dMH5KcPlnzxFXts+MBGaIB9fr7X2LqxJNoqZ/ErnfeHVC73tl9hGX3baRhSg1tTXXMnTYp3hEYo3Sb5atoO/rMbJmZbTSzjV1dXYUujlSQbJ69ZM0bp82YnLTzrvNgH9u7enmt89CwnYdhpAOV4pXvccqdZtbo7h1m1gjsS3Wgu68EVgK0t7erR0PyJptnL1nzhjtJZ+8dP+FceueTfHVBy7CJ8cNIByrFK9815YeAJcHnJcDaPP++SOgiEedQ33EOvHucQ339NJ08fkhN97Yrz+bmtdEmjfs37Y4PiYvtH1wTHq7JRMpLaDVlM/sF0U696Wa2G/g2cCuwxsyWAruAq8L6fZFCSLZy9C2L5/PZs97HuoSabvfho+zsPgJE19C773c7WXpBC2fPmkJrw2TVhCtYmKMvvphi18KwflOk0JKtHH3Tg1tonTGJtqa6AaMlEpssOnr6uPep7axbvkAjKipc0Xb0iZSS2Cy+N985krTTbm/PwBl/7vCDz7exYuGpNNbWqPNO4pSQSCRLiUmGUnXazaytGXJsrHnj+587i/OaT6Z5qposRDVlkawlzuJL1ml3y+L5zGusHXIsRGvRNz6wmYijgCyAasoiWUucxZfYaXdm42Rm141nXmMt1dVVQ46N0ew8SaSaskiWBs/ii3XandE4hbamunhATnYsaHaeDKSgLJKhwak5m+smDBiHHMtdEZuxl5jNTbPzZCRqvhDJQKqVRy45o4F1yxfw9uGj7DnQx7L7NiZdmUSz82QkqimLZGC41JxvHz5G16FjbO/qpW7CuAH7N+85EK8xa3aeDEc1ZZEMpErNuWnXAW5e+94svsR19fqOR3hy2372HOjTatQyItWURTIwYVx10tScsYAMA9fVg2i7cfO0iUpML2lRUBbJwLETJ+LjkBtra1i+8FROrZ+UdJhb89TxrFh4Kn+16HTeOvDukLX8RJJRUBbJwLSJJ7F64y5WLGzl6xedysontvPavt6kw9x2vX2Eu5/YztETkXj6Tg19k5EoKEs4qqoxs6xe1eNqsr7GrKbmnN7W3GkT+e7l85j3vil87+GXU87iW35Ra3w9vdvXvwagoW+SFnX0STgi/Vxz99NZXWL1dR/LyTVyKRJxug4dY9fb7yadxXf6zMm8uvfQkPX0Tp85mU+eNkOdfDIi1ZRFMhBLzRkJmiNiYrP4mqdOSLqe3hyNRZY0KSiLZCA2xC3VaiHzGqdoxp5kpSDNF2a2CLgDGAPc4+63FqIcIplqrB1PzdiqAU0WY6rgE631nNdcpxl7krW815TNbAzwt8CfAGcCXzSzM/NdDpHROHlCNd/+zLx4YL73qe001o6nfvK4eODVjD3JRiFqyh8GXnf37QBm9o/A5cDLBSiLSEbeOtDHL57Zyf/7+TaOHOtn/Lhq7nniDU6ZPoE505R6U7JXiKA8C3gz4ftu4CMFKIdIxhqm1PDavl6W/+L5+DaNP5ZcKkRHX7K/5XzIQWbLzGyjmW3s6urKQ7FEooZ79pR6U8JWiJrybqAp4fts4K3BB7n7SmAlQHt7+5CgLRKW4Z49deRJ2AoRlJ8FWs3sFGAP8AXgSwUoh8ioxDrytHyThCHvQdnd+83s68CviA6J+7G7b813OUREilFBxim7+zpgXSF+W0SkmJl78TfXmlkXsDNh03Rgf4GKk0u6j8La7+6LhjsgybOXqFTvezjleE9QfPeV8tkriaA8mJltdPf2QpcjW7qP0laO912O9wSldV/KfSEiUkQUlEVEikipBuWVhS5Ajug+Sls53nc53hOU0H2VZJuyiEi5KtWasohIWVJQFhEpIiURlBctWuREkxbppVcuXyPSs6dXSK+USiIo799fTGO+pZLo2ZN8K4mgLCJSKRSURUSKSEESEolkKhJxdnQfpvNgHw1TlMNYypeCshS9SMR5ZOtevrnmBfqOR+KrfSyaN1OBWcpOqM0XZrbDzDab2QtmtjHYNtXM1pvZtuC9LswySOnb0X04HpAB+o5H+OaaF9jRfbjAJRPJvXy0KX/K3c9JyNB0A7DB3VuBDcF3kZQ6D/bFA3JM3/EI+w71FahEUbOamjGzrF6zmpoLeg9SfArRfHE5cGHweRXwOHB9AcohJaJhSg01Y6sGBOZiWEH6rd1vcs3dT2d1jdXXfSxHpZFyEXZN2YFHzWyTmS0LtjW4ewdA8D4j5DJIiRvNCtKRiLO9q5ffvrGf7V29RCLDjtcXKRph15Q/7u5vmdkMYL2ZvZruiUEQXwbQ3Kw/8SpZpitIZ9sxqGdPCinUmrK7vxW87wMeAD4MdJpZI0Dwvi/FuSvdvd3d2+vr68MsppSA2ArS57dMp6V+0rDBNduOQT17UkihBWUzm2hmk2OfgUuALcBDwJLgsCXA2rDKIJWpWDsGRdIRZvNFA/CAmcV+5+fu/oiZPQusMbOlwC7gqhDLIBWoWDsGRdIRWlB29+1AW5Lt3cDCsH5XJNYxOLhNebiOQZFioRl9UnYy7RgUKSYKylKWYh2DLfWTCl0UkYwoS5yISBFRUBYRKSIKyiIiRURtypI3yoksMjIFZckL5UQWSY+aLyQvlBNZJD0KypIXmvoskh4FZcmL2NTnRJr6LDKUgrLkxWhyIotUInX0SV5UVRmXnNHA6mXn09HTR2NtDfMaa9XJJzKIgrLkRSTiPPpKp0ZfiIxAzReSFxp9IZIeBWXJC42+EEmPgrLkhUZfiKRHQVnyQqMvRNKjjj7JCyWeF0lP6EHZzMYAG4E97n6ZmU0FVgNzgR3A1e7+TtjlkMJT4nmRkeWj+WIF8ErC9xuADe7eCmwIvouICCEHZTObDXwauCdh8+XAquDzKmBxmGUQESklYdeUfwj8JZA4FqrB3TsAgvcZIZdBRKRkhBaUzewyYJ+7bxrl+cvMbKOZbezq6spx6URS07MnhRRmTfnjwGfNbAfwj8BFZvYzoNPMGgGC933JTnb3le7e7u7t9fX1IRZTZCA9e1JIoQVld/8rd5/t7nOBLwCPufuXgYeAJcFhS4C1YZVBpBLMamrGzLJ6zWpqLvRtSKAQ45RvBdaY2VJgF3BVAcogUjbe2v0m19z9dFbXWH3dx3JUGslWXoKyuz8OPB587gYW5uN3RURKjaZZi4gUEQVlEZEioqAsIlJElJBIMhKJODu6D9N5sI+GKUoqJJJrCsqStkjEeWTrXi3pJBIiNV9I2rSkk0j4FJQlbVrSSSR8CsqSNi3pJBI+BWVJm5Z0EgmfOvokbVrSSSR8CsqSES3pJBIuBWUB0h9/rHHKIuFSUJa0xx9rnLJI+NTRJ2mPP9Y4ZZHwKShL2uOPNU5ZJHwKypL2+GONUxYJn9qUhbnTJnLXl87lpd09RBzGGJw1u3bI+OPYOOXENuXbrjyb7sNH4/vVtiySHQVlAeBYv7Pyie0DOvAGSxyn3Hmwj+MnnJvXbmZn9xF1+onkSNrNF2Y2x8wuDj6PN7PJIxxfY2a/N7MXzWyrmX0n2D7VzNab2bbgvS67W5BsZdKBFxun3DClhmX3bWRn95ERzxGR9KUVlM3sPwH/DNwdbJoNPDjCaUeBi9y9DTgHWGRm5wM3ABvcvRXYEHyXPIpEnO1dvfz2jf1s7+odVQeeOv1EwpFu88XXgA8DzwC4+zYzmzHcCe7uQG/wdWzwcuBy4MJg+yqiC6pen0mhZfSSjTX+0bXt1IytGhBkR+rAi3X6ZXKOiIws3eaLo+5+LPbFzKqJBthhmdkYM3sB2Aesd/dngAZ37wAI3ocN7pJbyZoqblq7mduuPDujRENKTiQSjnRryr8xsxuB8Wb2R8CfAf8y0knufgI4x8xOBh4ws/npFszMlgHLAJqbm9M9TUaQrNlhZ/cRZp1cw7oMEg2Vc3KivD57VdWYlf6/meROukH5BmApsBm4DlgH3JPuj7j7ATN7HFgEdJpZo7t3mFkj0Vp0snNWAisB2tvbR6yVS3pSNTtMnXhSxomGyjU5UV6fvUg/19z9dFaXWH3dx3JUGCkG6TZfjAd+7O5XufvngR8H21Iys/qghoyZjQcuBl4FHgKWBIctAdaOotwySmp2EClu6daUNxANqrGOu/HAo8Bw/xfdCKwyszFEg/8ad3/YzH4LrDGzpcAu4KpRlVxGpZybHUTKQbpBucbdYwEZd+81swnDneDuLwHnJtneDSzMqJSSU+Xa7CBSDtINyofN7Dx3fw7AzD4IHAmvWDIa/f0Rtnb00NHTR2PteOY1TqG6WulNREpJukH5G8A/mdlbwfdG4JpQSiSj0t8f4cEX93DTg1vi449vWTyfxW2zFJhFSkhaQdndnzWz04EPAAa86u7HQy2ZZGRrR088IEMw/vjBLbTOmERbk2ayi5SKYYOymV3k7o+Z2RWDdrWaGe7+yxDLJhno6Ek+7XlvTx9tTZldS0s+iRTOSDXlTwKPAZ9Jss8BBeUi0Vg7Pun445m1mU171pJPIoU1bFB2928HH78azM6TAkin5jqvcQq3LJ4/pE15XmNtRr+VKmPc6csXaLSGSB6k29H3BzN7BFgNPBYkG5I8SLfmWl1dxeK2WbTOmMTenj5m1tYwr7E2406+4bK/KSiLhC/d/2I/APwb0WxxfzCzu8zsgvCKJTGZ5Dqurq6iramOP57fSFtT3ahGXWjJJ5HCSuu/Wnc/4u5r3P0KohNCpgC/CbVkAgytuTbW1rD0ghZe6zzE9q5eIpHc/tGiadgihZX2clBm9kmiY5P/BHgWuDqsQsl7EhMINdbWcO35c7jzsW2hdcJpGrZIYaW78sgfiE4geRKY7+5Xu/v9YRZMohJrrlecNzsekCG8JZhi07DPb5lOS/0kBWSRPBqxphwkFPp7d/9uHspT8ZKNtIjVXF/rPJS0E67zYHQJpsRzAI01FilBIwZldz9hZp8CFJRDNtxIi9jIh2RjkY+fcC6988kB54yrNr7+8+c11likxKTbPf90MOJigZmdF3uFWrIKlGqkxa63D7O9q5fuw0eHLNt025Vnc/PazUPOeWl3T+jNHCKSe+l29MXyJifWlh24KLfFqWzJxgjXTRjHc7sOcOMD0cA7Z9p4Vl7bztgxRsOUGroPH2Vn98CEfX3HIwwelKGxxiKlId2ERJ8KuyCSfKmmq9pnxwMyRNfTW3bfRtYlzLBL1qQxuJVCY41FSkO6oy8azOxeM/vX4PuZwcohkiORiOMOP/h8GysWnkpjbTRAnzZjcsoZdpB6XPHZs2s11likBKXbfPET4O+B/xZ8f43olOt7QyhTxUnWwff9z53Fec0ncyKSvCYcq/WmGlcMZLQ6tYgUh3Q7+qa7+xogAuDu/cCwCYrMrMnMfm1mr5jZVjNbEWyfambrzWxb8F7xyX6TdfDd+MBmIg6nTB95hl2yccUaayxSmjJZDmoa0c49zOx8oGeEc/qBv3D358xsMrDJzNYDfwpscPdbzewG4Abg+lGVvkTFxiJ3Hz7KuDFVKXMh7+w+PGCcsmq9IuUv3ZryN4GHgPeb2b8DPwX+fLgT3L0jtqafux8CXgFmAZcDq4LDVgGLMy926Yo1VfyHn/yeZ//wDtes/B1b3jqYNAnQ828e4JGtewFU65VwVVVjZlm9ZjU1F/ouykK6NeX3E8150QRcCXwkg3Mxs7lEExk9AzS4ewdEA7eZzcikwKUu1lSx9IKW+JTp+zftZvlFrQNyWiy/qJX7freTd949plzGEr5IP9fc/XRWl1h93cdGPkhGlG5gvdnd/ylo/70Y+Gvg74gG52GZ2STgfuAb7n7QLL1anpktA5YBNDeXz/8Dx8YimxFvsujo6eO+3+1k6QUtnNYwEbMqduw/zJUfnM39m3bz9uGj8XOHm0adbNtoatXJpnrn6tqloFyfPSkN6QblWKfep4H/5e5rzez/GekkMxtLNCD/Q8J6fp1m1hjUkhuBfcnOdfeVwEqA9vb2skmqn5ivOHFURUdPHw+/tIdln3g/33t4c7zG/M0/Oo39vcf48r2/j2+760vncqzfh0zHzsXU6lRTvStp2na5PntSGtJtU95jZncTTde5zsxOGulci1aJ7wVecffbE3Y9BCwJPi8B1mZW5NIQiTjbu3p5ett+nv1DN4++vJdNO97mfZNruP3qc/iXF/ew/KLWAQH6e5efxfcefnnAKIzb17/Gyx0HB2x7aXdP0unYuZhanWqqt6Zti+RHujXlq4FFwA/c/UBQw/2/Rzjn48C1wGYzeyHYdiNwK7AmmHyyC7gq41IXuWS1zeUXtfLfN+7ia59qZe70Gi4/ZxZVVdHJIlYFpzdMYd+h5KMwBk+ZjjhpHTeaqdWploPStG2R/Eh3mvW7JKxcHXTUdYxwzlNAqr9tF6ZbwFKUrLZ552PbWHpBC99au4WV136QOze8Hj++ZmwV65YvSDrNOtmU6TEW3tTqdMugadsi4Uh7BIWkr/NgH3UTxnHFebOJ9Wvev2l3vHPvnXeP87VPnTpg375DfXx47jRuv/qcpO25sUBZM7aKs2bXpnXcaKZWx6Zth3FtERmZgnIIZk6p4SsfncMdG94b4rZiYSs11VVBDfMkrr//pQH7Zk6pyWjKNBDK1GpN2xYpLAXlEBzqOx4PyBCtHd+xYRs/vPocvvvZ+fz9v78xZN8lZ84E3psyPbitNpttmcqkDCKSW5mvQS8jeivFtOkT7pzeOIlHX94/ZF9Xb18+iygiRUpBOQSNteOTTpueXTeeSSeNTbpPnWYiAgrKoZjXOIVbFs8fMAb5lsXzmddYmzL/cazdNja++bdv7OeNfb3s2B/9vL2rl8jgcWkiUnbUphyC6uoqFrfNonXGJPb29DGztoZ5jbVUV0cDcaqsb8nGN69Y2MpPfxvNgVHOs+hEJEo15ZBUV1fR1lTHH89vpK2pLh6QIXn+Y0g+vvmODdu44rzZmkUnUiEUlAsgsYkisVki1Wy62HjmxGWg0rmeiJQeNV/kWaqEP4vmzUw5m879vc+DOwSHu56aOURKj2rKeZYq4c+OYJWRwZ2AKxa28svndqecRTfc9USk9KimnGepmihiyX0SOwHrJ9UwpgrObT455Sy6ka4nIqVFQTnPUjVRJK5OPXjm3NzpqYPrSNcTkdKi5os8G2mccqGvJyKFpZpynqVK+DPaTrlcX09ECktBuQBSJfwpluuJSOEoKA8j2QKi6dZAszlXRCqXgnIK2Yz/1dhhERmt0Dr6zOzHZrbPzLYkbJtqZuvNbFvwXhfW72crm/G/GjssFamqGjPL6jWrqbnQd1FwYdaUfwLcBfw0YdsNwAZ3v9XMbgi+Xx9iGUYtcfxvY21NfGmnd949xhv7etl3KHWzRKpzu3qPqhlDylekn2vufjqrS6y+7mM5KkzpCi0ou/sTZjZ30ObLgQuDz6uAxynSoBwb/1s3YRzXnj+HOx/bRt2EcUwcN2bAMk/JmiWSndt3PMI9T25XM4aIDCvf45QbgpWwYytiz8jz76ctNv73qvbZ8aB6xXmzhyzzlKxZItm5wx0vIhJTtJNHzGyZmW00s41dXV15//3Y+N9zmk6mbsI4vvapU2muG89XF7TQWPvebLlkmdsSz001BVqKV6GfPals+Q7KnWbWCBC870t1oLuvdPd2d2+vr6/PWwETVVUZLdMn8pWPzuHep7Zz/S83c8+T27n2/DnxwJxqSnNVlTF32kQt/VSCiuHZk8qV76D8ELAk+LwEWJvn3x/R4NzE/Sd8SJPFnY9FE8+PNKU51RTo5roJyn8sIkmF1tFnZr8g2qk33cx2A98GbgXWmNlSYBdwVVi/PxrJxhf/4PNtSZsgmqeOZ9knWhhXnbrDLtkU6Oa6CTz6SqfGMItIUmGOvvhiil0Lw/rNbCUbX7xt36GkWdh2vX2Ev/3169SMrWLd8gUppzgPngK9vas36Rjm04e5hohUjqLt6Mu32LTowbXiNRt3c/NlZw5oglh+UStPvraPr33qVL66oIWu3qMjNkHEmkVe6zyU884/LQclUj40zZr3mi3+z96DQ2rF77x7jMN9x1l6QQvNU8ez58ARHtnSwaL5jWmPP05sFvnqgpac5j/WlG6R8qKaMu81W6zZuJvlF7UO6ZhrmTGJe5/azg//bRvjx47hwtNnZDT+OLFZ5P5NyX9jtPmPNaVbpLxUZE15cAa37sNH6TseoaOnj/t+t5OlF7RgBgtOnc6H5k4lEnFWLzufjp4+ZteNZ9/BoxktwdR5sI+6CePi060dZ8XCVlqmT6S1YXJWU6+1HJRIeam4oJzsz/3brjybOdPGs7P7CB09ffEOvCvOnQUwZLTEj65tz6gJorG2hq98dM6A6dkrFrbygZmTh13qKR1aDkqkvFRc80WyP/evv/8lvnf5WdSMraKxtoblC0/lB59vwx12vT30+JvWbua2K89OuwniRIQhY53v2LCNE5Gkh2dEy0GJlJeKqymn+nN/7BjjkRULeG7XAW58YHO8Rvv9z51F3YRxdPS8NzpiZ/cRZp1cw7o0l2Dadyj5b3b19vH+GdnVlLUclEh5qbiacuzP/UQ1Y6tomFJDxIkHZIgGzhsf2MxV7bOHHD914km01E/i/JbptNRPGjYIpvrNXDUxxMZCp1MWESluZRmUhxu3O9yf+6lq0ac1TM6qeUBNDCKSrrJrvhhp3O5wf+6n6jQ7Y+aUtJsqklETg4ikq+xqyumM2031536qGu0p0ydm3TygJgaRNBTJklKzmpoLVo6yqilHIk7XoaP82YWncsr0iew58C4A/Sec1zoPAQyoofb3R9ja0UNHTx+NteOZ1zhlQI22flINY6rgmT90azVrkXwokiWl3tr9ZsHKUTZBOVmzxX+5+DTGj63i+//26pCmjEjEefDFPdz04Jb4vlsWz2dx2yxa6icxd9pErWYtInlXNs0XyZot/r9/e439h48lbcrY2tETD8ixfTc9uIWtHT0pr6fVrEUkbGVTU061gnTrjMk01tbExxn3HY/QebCPniPHk4602NvTR1tTdtOXNfVZREarbIJyqhWkY6k27/vdTjp6+qgZW8XxE84rHUMzwtWMrWJmsMxTNtOXNfVZREarbJovhltBOnH5ptuuPJub125OmhHulsXzmddYO+B6oxlbrHHJIjJaZVNTBhhXbcw6eXzSpoMzZk5m3fIFdB8+ys7uIwADMsJ9tGUqH5k7jerqaCDNZmyxxiWLyGgVJCib2SLgDmAMcI+735rtNXd0H+brP38+ZRL5mbU18fbc2P7BGeFiATlm8FJOmcjmXBGpXHlvvjCzMcDfAn8CnAl80czOzPQ6sanUz+96m4073ubljoMpk8jfsvgsIh49vrluQsZNC1puSUTypRA15Q8Dr7v7dgAz+0fgcuDldC8QGwf846fe4MrzmvnOw1vjNeTERPVjquAjp0zlxgc2s7P7SDwAX3JGQ9rTpjXmWETyqRAdfbOANxO+7w62pS02DvgrH2vhOw9vHVJD7ujp496nttMwpSYekOG98cK73nk37SnPGnMsIvlUiJpysgg4pD3AzJYBywCamwfOIY+NAz5ytD8eLBNryKc1TOK1zl4O9R2PB+SYTMcLa8xx5Rnu2RMJWyFqyruBpoTvs4G3Bh/k7ivdvd3d2+vr6wfsi40DnnBS9YA8xbEa8hgz/vbXr9N79ETWeYzDzoUsxWe4Z09KQA6SGhVSIWrKzwKtZnYKsAf4AvClTC4QGwf846fe4NuXzYs3YcTGGk8eP4aasVXcv2k3Kxa2Dlgbb7S5kAe3KWvMsUiRKpKkRqOV96Ds7v1m9nXgV0SHxP3Y3bdmco34OOCZkzl45Bg/W/oR9vcepbG2hnmNtVRVWbwjb+aUGi45cyZdvcqFLCLFryDjlN19HbAum2vExgGnMniMcDZr4WnMsYjkS9lMsxYRKQcKyiIiRcTci392mpl1ATsTNk0H9heoOLmk+yis/e6+aLgDkjx7iUr1vodTjvcExXdfKZ+9kgjKg5nZRndvL3Q5sqX7KG3leN/leE9QWvel5gsRkSKioCwiUkRKNSivLHQBckT3UdrK8b7L8Z6ghO6rJNuURUTKVanWlEVEylLJBWUzW2Rm/8fMXjezGwpdnnSYWZOZ/drMXjGzrWa2Itg+1czWm9m24L2u0GVNh5mNMbPnzezh4HtJ3sdoleIzmEy5PZeJSvkZLamgnKtVSwqgH/gLdz8DOB/4WlDuG4AN7t4KbAi+l4IVwCsJ30v1PjJWws9gMuX2XCYq2We0pIIyCauWuPsxILZqSVFz9w53fy74fIjowzKLaNlXBYetAhYXpIAZMLPZwKeBexI2l9x9ZKEkn8Fkyum5TFTqz2ipBeWsVy0pNDObC5wLPAM0uHsHRP8DAWYUsGjp+iHwl0Bi5v9SvI/RKvlnMJkyeC4T/ZASfkZLLSintWpJsTKzScD9wDfc/WChy5MpM7sM2OfumwpdlgIq6WcwmVJ/LhOVwzNakNSdWUhr1ZJiZGZjiT74/+Duvww2d5pZo7t3mFkjsK9wJUzLx4HPmtmlQA0wxcx+RundRzZK9hlMpkyey0Ql/4yWWk05vmqJmY0jumrJQwUu04gsur7MvcAr7n57wq6HgCXB5yXA2nyXLRPu/lfuPtvd5xL9t3/M3b9Mid1HlkryGUymXJ7LROXwjJZUTTkXq5YUyMeBa4HNZvZCsO1G4FZgjZktBXYBVxWmeFkrl/sYUQk/g8mU+3OZqGTuSTP6RESKSKk1X4iIlDUFZRGRIqKgLCJSRBSURUSKiIKyiEgRUVAuA2a2w8ym5+o4kVwws++a2cWFLkepKalxyiJSXMys2t37k+1z92/luzzlQDXlEmJmc83sVTNbZWYvmdk/m9mEYPefm9lzZrbZzE4Pjp9mZo8GeWXvJnneBhHMbKKZ/W8ze9HMtpjZNWb2QTP7jZltMrNfBdOTMbPHzez7ZvYb4L8Ff4FVBfsmmNmbZjbWzH5iZp8Ptn/IzJ4Orv97M5sc5Dz+n2b2bPA8X1fAf4KioaBcej4ArHT3s4GDwJ8F2/e7+3nA3wH/Ndj2beApdz+X6DTT5nwXVkrGIuAtd29z9/nAI8DfAJ939w8CPwb+e8LxJ7v7J939O8CLwCeD7Z8BfuXux2MHBtPRVwMr3L0NuBg4AiwFetz9Q8CHgP9kZqeEepclQEG59Lzp7v8efP4ZcEHwOZZMZhMwN/j8ieAY3P1/A+/kqYxSejYDF5vZbWa2gGjSpfnA+mAK9k1Eky/FrB70+Zrg8xcG7YNoRaLD3Z8FcPeDQZPHJcBXgus/A0wDWnN5U6VIbcqlZ/C8+Nj3o8H7CQb+76p59DIid3/NzD4IXAr8D2A9sNXdP5rilMMJnx8C/oeZTQU+CDw26Fgj+XNowJ+7+6+yKnyZUU259DSbWew/lC8CTw1z7BPA/wVgZn8CFO26ZFJYZvY+4F13/xnwA+AjQH3sWQvaiOclO9fde4HfA3cAD7v7iUGHvAq8z8w+FFxrsplVE03q9J+D9KGY2WlmNjGE2yspqimXnleAJUHH3Taibch/nuLY7wC/MLPngN8QzY4lksxZwP80swhwHPjPRNfwu9PMaonGih8CqTLirQb+Cbhw8A53P2Zm1wB/Y2bjibYnX0x0uaa5wHNBGtEuiniZpnxRlrgSEizZ83DQESMiZUjNFyIiRUQ1ZRGRIqKasohIEVFQFhEpIgrKIiJFREFZRKSIKCiLiBQRBWURkSLy/wOl+doavYjLlwAAAABJRU5ErkJggg==\n",
      "text/plain": [
       "<Figure size 360x360 with 6 Axes>"
      ]
     },
     "metadata": {
      "needs_background": "light"
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "sns.pairplot(df.iloc[:,0:4])"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 35,
   "id": "711bfeaf",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "<seaborn.axisgrid.PairGrid at 0x1c72a095b50>"
      ]
     },
     "execution_count": 35,
     "metadata": {},
     "output_type": "execute_result"
    },
    {
     "data": {
      "image/png": "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\n",
      "text/plain": [
       "<Figure size 540x540 with 12 Axes>"
      ]
     },
     "metadata": {
      "needs_background": "light"
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "sns.pairplot(df)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 36,
   "id": "dd387d73",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "<matplotlib.collections.PathCollection at 0x1c72a700400>"
      ]
     },
     "execution_count": 36,
     "metadata": {},
     "output_type": "execute_result"
    },
    {
     "data": {
      "image/png": "iVBORw0KGgoAAAANSUhEUgAAAXMAAAD4CAYAAAAeugY9AAAAOXRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjMuNCwgaHR0cHM6Ly9tYXRwbG90bGliLm9yZy8QVMy6AAAACXBIWXMAAAsTAAALEwEAmpwYAAAT80lEQVR4nO3df4xVdXrH8c/jOC5XahjRQWFkmDWd4FqnK/GuYEk2sC6LzZpl1qqV1IZNTfjHttvY0kBL2qRLCy2N7abZpEu2ppPSoqbVkWy3SwlCTbcLdSjWWSuE1vLDgRX8MXZXxhXHp3/MueMA9849h3vume85834l5t7zzDmcb/zjM2e+53vOY+4uAEC+XTHVAwAANI4wB4ACIMwBoAAIcwAoAMIcAArgyixPdv3113tXV1eWpwSA3Dt48OCb7t4+2T6ZhnlXV5cGBgayPCUA5J6ZHa+3D9MsAFAAhDkAFABhDgAFQJgDQAEQ5gBQAJmuZrkc/YeGtHXXEZ0aHtG8tpLWrVyo3kUdUz0sAAhK0GHef2hIG54Z1Mj5UUnS0PCINjwzKEkEOgBMEPQ0y9ZdR8aDvGLk/Ki27joyRSMCgDAFHeanhkcS1QFgugo6zOe1lRLVAWC6CjrM161cqFJrywW1UmuL1q1cOEUjAoAwBX0DtHKTk9UsADC5oMNcGgt0whsAJhf0NAsAIB7CHAAKgDAHgAIgzAGgAAhzACgAwhwACoAwB4ACIMwBoAAIcwAoAMIcAAog+Mf56TQEAPUFHeZ0GgKAeIKeZqHTEADEE3SY02kIAOKJFeZmdszMBs3sJTMbiGqzzWy3mR2NPq9Ne3B0GgKAeJJcmS9399vdvRxtr5e0x927Je2JtlNFpyEAiKeRaZZVkvqi732SehsezUV6F3Vo83096mgrySR1tJW0+b4ebn4CwEXM3evvZPa/kt6R5JK+6e7bzGzY3dsm7POOu18y1WJmayWtlaTOzs47jh8/ntbYAWBaMLODE2ZFqoq7NHGpu58yszmSdpvZ4biDcPdtkrZJUrlcrv+bAwCQWKxpFnc/FX2ekfSspDslvWFmcyUp+jzTrEECACZXN8zNbKaZXVP5LukLkn4gaaekNdFuayQ916xBAgAmF2ea5QZJz5pZZf+/c/fvmtmLkp42s0cknZD0QPOGCQCYTN0wd/fXJH26Sv0tSXc3Y1AAgGSCfgIUABAPYQ4ABUCYA0ABEOYAUACEOQAUAGEOAAVAmANAARDmAFAAhDkAFEDQDZ0laWP/oHYcOKlRd7WYafXi+drU2zPVwwKAoAQd5hv7B7V9/4nx7VH38W0CHQA+FvQ0y44DJxPVAWC6CjrMR2t0QapVB4DpKugwbxl77W7sOgBMV0GH+erF8xPVAWC6CvoGaOUmJ6tZAGBy5hnOP5fLZR8YGMjsfABQBGZ20N3Lk+0T9DQLACAewhwACoAwB4ACIMwBoAAIcwAoAMIcAAqAMAeAAiDMAaAACHMAKADCHAAKIPa7WcysRdKApCF3v9fMZkt6SlKXpGOSHnT3d9IeYP+hIW3ddUSnhkc0r62kdSsXqndRR9qnAYBcS3Jl/lVJr07YXi9pj7t3S9oTbaeq/9CQNjwzqKHhEbmkoeERbXhmUP2HhtI+FQDkWqwwN7ObJH1R0rcmlFdJ6ou+90nqTXVkkrbuOqKR86MX1EbOj2rrriNpnwoAci3uNMufS/ptSddMqN3g7qclyd1Pm9mcagea2VpJayWps7Mz0eBODY8kqgNAaLKaKq57ZW5m90o64+4HL+cE7r7N3cvuXm5vb0907KxSa6I6AIQky6niONMsSyV9ycyOSXpS0ufMbLukN8xsriRFn2fSHlyt7nB0jQOQB1lOFdcNc3ff4O43uXuXpIckPe/uD0vaKWlNtNsaSc+lPbjhc+cT1QEgJFlOFTeyznyLpBVmdlTSimg7VfPaSonqABCSLDMsUZi7+z53vzf6/pa73+3u3dHn22kPbvkt1efYa9UBICTrVi5UqbXlglqptUXrVi5M/VxBN3Tee/hsojoAhKSyaiWL1SxBhzlLEwHkXe+ijkyeWg/63SzMmQNAPEGHeZbzTQCQZ0FPs2Q53wQAeRZ0mEvZzTcBQDNs7B/UjgMnNequFjOtXjxfm3p7Uj9P8GEOAHm1sX9Q2/efGN8edR/fTjvQg54zB4A823HgZKJ6IwhzAGiSUfdE9UYEP82S1XwTAKStxaxqcLc04W2BQV+ZV+abKv8zKvNNG/sHp3hkAFDf6sXzE9UbEXSYZznfBABp29Tbo4eXdI5fibeY6eElndNvNUuW800A0AybensymRoO+sq81rxSM+abACDPgg7zLOebACDPgp5mqfxpwmoWAJhc0FfmklReMFs3zpohk3TjrBkqL5g91UMCgOAEfWVe6WxdaYha6Wwtife1AMAEQV+ZZ9nZGgDyLOgwp9MQAMQTdJjTaQgA4gk6zOk0BADxBH0DlE5DABBP0GEu0WkIAOIIepoFABAPYQ4ABUCYA0AB1J0zN7MZkl6Q9Ilo/7939983s9mSnpLUJemYpAfd/Z20B9h/aIgboABQR5wr859I+py7f1rS7ZLuMbMlktZL2uPu3ZL2RNupqjzOPzQ8ItfHj/P3HxpK+1QAkGt1w9zH/DjabI3+c0mrJPVF9T5JvWkPjsf5ASCeWEsTzaxF0kFJPy3pG+5+wMxucPfTkuTup81sTo1j10paK0mdnZ2JBsfj/ADyLqup4lg3QN191N1vl3STpDvN7La4J3D3be5edvdye3t7osFdfVVLojoAhCTLqeJEq1ncfVjSPkn3SHrDzOZKUvR5Ju3BnftgNFEdAEKS5VRx3TA3s3Yza4u+lyR9XtJhSTslrYl2WyPpubQHV6ttM+2cAeRBllPFcebM50rqi+bNr5D0tLt/28y+L+lpM3tE0glJD6Q9uBYzjfql0U1DZwB5MK+tpKEqwd2MN7/WDXN3f1nSoir1tyTdnfqIJlhy87X63v+8XbUOAKHruq56mHddl36YB/0E6LG3qv8pUqsOACHZ/1r15yhr1RsRdJizNBFAnlWbJp6s3oigw7zt6tZEdQAISa37e8247xd0mNf65dWEX2oAkLrVi+cnqjci6OYU746cT1QHgJBs6u2RJO04cFKj7mox0+rF88fraQr6ypyGzgDyrrxgtm6cNUMm6cZZM1ReMLsp5wk6zGnoDCDPgn2cP2u9izq0+b4edbSVZJI62krafF8P7zMHkAtZPs4f9Jy5RENnAPkV2uP8U4pOQwDyKsvH+YOeZqHTEIA8q/XY/rR7nJ9OQwDyjMf5IzzODyDPeJw/wjpzAHlW66H9ZrzEO+gwZ505gDzLsvVl0KtZKqtWWM0CII+ybH0Z9JW5JA0cf1s/fPd9uaQfvvu+Bo5f2qwCAEKU5VRx0GG+sX9Q2/efGL9ZMOqu7ftPaGP/4BSPDADqY2liZMeBk4nqABASliZGslzWAwBpY2liJMtlPQCQNjoNRbJc1gMAaaPTUCTLZT0AkLYsOw0FHeZZvnEMAJphU29PU8L7YkFPsyy/pT1RHQCmq6DDfO/hs4nqADBd1Q1zM5tvZnvN7FUze8XMvhrVZ5vZbjM7Gn1em/bgeGsiAMQT58r8Q0m/6e6fkrRE0qNmdquk9ZL2uHu3pD3Rdqp4ayKAvOs/NKSlW57XJ9f/o5Zueb5pzXXqhrm7n3b3/4i+/0jSq5I6JK2S1Bft1iepN+3BfThafdVKrToAhCTLbmmJ5szNrEvSIkkHJN3g7qelscCXNCftwb3xow8S1QEgJFl2S4sd5mb2U5L+QdJvuPv/JThurZkNmNnA2bPcuAQwfWR53y9WmJtZq8aC/G/d/Zmo/IaZzY1+PlfSmWrHuvs2dy+7e7m9nSWFAKaPWaXWRPVGxFnNYpL+StKr7v74hB/tlLQm+r5G0nNpD66lxusLatUBICS1XsHShFezxHoCdKmkX5Y0aGYvRbXfkbRF0tNm9oikE5IeSHtwH9V4sVitOgCEZPjc+UT1RtQNc3f/V9V+UeHd6Q7nQjzODyDPssywoJ8AzbJLBwCkjU5DkSy7dABA2ug0FKHTEIA8o9NQJMs7wQCQZ0GHeenK6sOrVQeA6SroVBw5/1GiOgBMV0GHOW9NBIB4gg7zdSsXqtR6YfPmUmuL1q1cOEUjAoD4uufMTFRvRNBh3ruoQ5vv61FHW0kmqaOtpM339ah3UcdUDw0A6tr92LJLgrt7zkztfmxZ6ucyz3CZX7lc9oGBgczOBwBFYGYH3b082T5BX5kDAOIhzAGgAAhzACiAOK/ABQBcpv5DQ9q664hODY9oXltJ61YubMoiDsIcAJqk0tC50ge00tBZUuqBzjQLADRJkA2dAQDJBNfQGQCQXJavJCHMAaBJ6DQEAAWQZaeh4FezbOwf1I4DJzXqrhYzrV48X5t6e6Z6WABQV5adhoIO8439g9q+/8T49qj7+DaBDgAfC3qaZceBk4nqADBdBR3mNHQGgHiCDvOWGp2ba9UBYLoKOsxXL56fqA4AIbnhmqsS1RsR9A3Qyk1OVrMAyKM3f3w+Ub0RdcPczJ6QdK+kM+5+W1SbLekpSV2Sjkl60N3TXzipsUAnvAHkUZb3/eJMs/y1pHsuqq2XtMfduyXtibYBABNked+vbpi7+wuS3r6ovEpSX/S9T1JvusMCgPy7uf3qRPVGXO4N0Bvc/bQkRZ9z0hsSABTDa2fPJao3ouk3QM1sraS1ktTZ2Zn4+Ky6dABA2kKbM6/mDTObK0nR55laO7r7Nncvu3u5vb090UkqXTqGhkfk+rhLR/+hocscNgBkJ6g58xp2SloTfV8j6bl0hnOhLLt0AEDasnxWpm6Ym9kOSd+XtNDMXjezRyRtkbTCzI5KWhFtpy7LLh0AkLZNvT16eEnn+JV4i5keXtLZlOXWdefM3X11jR/dnfJYLjGvraShKsHdjC4dANAM5QWztffwWZ0aHtGNs2aovGB2U84T9OP8y2+pPsdeqw4AIcnyvl/QYb738NlEdQAISZb3/YIOc+bMAeRZlhkWdJjPKrUmqgNASNqurp5VteqNCDrMay3F5HXmAPKg1rNBzeivE3SYD5+r/prIWnUACMm7I9Wzqla9EUGHea0liCxNBJAHWWZY0GG+buVClVpbLqiVWlu0buXCKRoRAMSXZYYF3Wmo8kItXrQFII+yzDDzDDvdl8tlHxgYyOx8AFAEZnbQ3cuT7RP0lTkA5N3G/sFM+hgT5gDQJBv7B7V9/4nx7VH38e20Az3oG6AAkGc7DpxMVG9E8FfmKx7fp6Nn3hvf7p4zU7sfWzZ1AwKAmPLQaSgTFwe5JB09855WPL5vagYEAIEKOswvDvJ6dQAISa03jzTjjSRBhzkA5FmtyZRmLAgnzAGgSfLQ0DkT3XNmJqoDQEhubr86Ub0RQYf57seWXRLcrGYBkBevnT2XqN6IoMNckh5d3q2OtpJMUkdbSY8u757qIQFALFkuTQx6nXmlGWqlh16lGaokXrYFIHhXmPRRldy+ognLWYK+Ms+yGSoApO0TV1aP2Fr1RgQd5jR0BpBn75//KFG9EUGHOZ2GAOQZnYYiy29pT1QHgJDQaSiy9/DZRHUACEmWnYYaCnMzu0fS1yW1SPqWu29JZVQR5swB5F3voo5MVt9d9jSLmbVI+oakn5d0q6TVZnZrWgOTmDMHgLgamTO/U9J/u/tr7v6BpCclrUpnWGOynG8CgDxrZJqlQ9LEdhmvS1rc2HAulOV8EwDkWSNhXu0ZpkuedTKztZLWSlJnZ2fik2Q13wQAedbINMvrkuZP2L5J0qmLd3L3be5edvdyeztLCgGgGRoJ8xcldZvZJ83sKkkPSdqZzrAAAElc9jSLu39oZr8qaZfGliY+4e6vpDYyAEBsDa0zd/fvSPpOSmMBAFymoB/nBwDEY96El6TXPJnZWUnHL/Pw6yW9meJwACBLjWTYAnefdAVJpmHeCDMbcPfyVI8DAC5HszOMaRYAKADCHAAKIE9hvm2qBwAADWhqhuVmzhwAUFuerswBADUQ5gBQAFMa5mbmZvY3E7avNLOzZvbtOsctq7cPAKTBzEbN7KUJ/3U18VzHzOz6yzl2qnuAvifpNjMrufuIpBWShqZ4TAAw0Yi73z7Vg6gnhGmWf5L0xej7akk7Kj8wszvN7N/M7FD0eUmLITObaWZPmNmL0X6pdjsCgIuZ2R1m9i9mdtDMdpnZ3Ki+z8z+zMxeMLNXzewzZvaMmR01s00Tju+Pjn0l6vlQ7RwPm9m/R38NfDNq1VlTCGH+pKSHzGyGpJ+VdGDCzw5L+qy7L5L0e5L+qMrxvyvpeXf/jKTlkraa2cwmjxnA9FGaMMXyrJm1SvoLSfe7+x2SnpD0hxP2/8DdPyvpLyU9J+lRSbdJ+oqZXRft8yvRsWVJvz6hLkkys09J+kVJS6O/CkYl/dJkg5zqaRa5+8vRHNRqXfoGxlmS+sysW2NdjFqr/BNfkPQlM/utaHuGpE5JrzZnxACmmQumWczsNo2F824zk8ZeAX56wv6Vvg6Dkl5x99PRca9prKHPWxoL8C9H+82X1B3VK+6WdIekF6NzlCSdmWyQUx7mkZ2S/lTSMkkTf0N9TdJed/9yFPj7qhxrkn7B3Y80eYwAII1lzivufleNn/8k+vxowvfK9pVmtkzS5yXd5e7nzGyfxi5CLz5Hn7tviDuoEKZZpLE/U/7A3Qcvqs/SxzdEv1Lj2F2Sfs2iX19mtqgpIwSAMUcktZvZXZJkZq1m9jMJjp8l6Z0oyG+RtKTKPnsk3W9mc6JzzDazBZP9o0GEubu/7u5fr/KjP5G02cy+p7E/Zar5msamX142sx9E2wDQFO7+gaT7Jf2xmf2npJck/VyCf+K7GrtCf1ljebW/yjn+S9JGSf8c7bdb0tzJ/lEe5weAAgjiyhwA0BjCHAAKgDAHgAIgzAGgAAhzACgAwhwACoAwB4AC+H9iNYEZPcdNvQAAAABJRU5ErkJggg==\n",
      "text/plain": [
       "<Figure size 432x288 with 1 Axes>"
      ]
     },
     "metadata": {
      "needs_background": "light"
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "plt.scatter(df.sex,df.phd)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 37,
   "id": "0dd1ab55",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(array([13.,  9., 13., 13., 13.,  5.,  7.,  1.,  2.,  2.]),\n",
       " array([ 1. ,  6.5, 12. , 17.5, 23. , 28.5, 34. , 39.5, 45. , 50.5, 56. ]),\n",
       " <BarContainer object of 10 artists>)"
      ]
     },
     "execution_count": 37,
     "metadata": {},
     "output_type": "execute_result"
    },
    {
     "data": {
      "image/png": "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\n",
      "text/plain": [
       "<Figure size 432x288 with 1 Axes>"
      ]
     },
     "metadata": {
      "needs_background": "light"
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "plt.hist(df['phd'])"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 40,
   "id": "fe2981f0",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(array([22., 26., 18.,  8.,  4.]),\n",
       " array([ 1., 12., 23., 34., 45., 56.]),\n",
       " <BarContainer object of 5 artists>)"
      ]
     },
     "execution_count": 40,
     "metadata": {},
     "output_type": "execute_result"
    },
    {
     "data": {
      "image/png": "iVBORw0KGgoAAAANSUhEUgAAAXAAAAD4CAYAAAD1jb0+AAAAOXRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjMuNCwgaHR0cHM6Ly9tYXRwbG90bGliLm9yZy8QVMy6AAAACXBIWXMAAAsTAAALEwEAmpwYAAAMdElEQVR4nO3df4jk9X3H8dernm5LFHr2Vjnu1G2DhEhJzt5ihSvlkjThYkM10ECFyv2RcPlDQcFQrPdH0sJB/mhM/ymBSz08qLEIapUS2hxXDxMotrv2Gk82wRDO653H7YoE7T8rp6/+Md9Nh82uMzu/33PPBywz85nZnffHw+cN35nvrZMIAFDPr417AABAbwg4ABRFwAGgKAIOAEURcAAoatson2zHjh2Zm5sb5VMCQHmLi4tvJZldvz7SgM/NzWlhYWGUTwkA5dl+Y6N1DqEAQFEEHACKIuAAUBQBB4CiCDgAFEXAAaAoAg4ARRFwACiKgANAUQR8gt2ye1W2rqivW3avjvs/O1DGSE+lx9acuzCjxSP7xz3GSO09fGrcIwBl8AocAIoi4ABQFAEHgKI6Btz2TbZftL1k+zXbDzbr37B9wfbp5uuu4Y8LAFjTzZuYlyU9nOQV29dJWrR9ornv20n+ZnjjAQA20zHgSS5Kuthcf9f2kqRdwx4MAPDhtnQM3PacpNslvdwsPWD7x7aP2d6+yfccsr1ge2FlZaW/aQEAv9R1wG1fK+kZSQ8leUfSdyR9VNIetV6hf2uj70tyNMl8kvnZ2V/5lW4AgB51FXDbV6sV7yeTPCtJSS4leT/JB5K+K+mO4Y0JAFivm0+hWNLjkpaSPNa2vrPtYV+UdGbw4wEANtPNp1D2SbpP0qu2Tzdrj0q61/YeSZF0VtJXhzAfAGAT3XwK5UeSvMFd3x/8OACAbnEmJgAURcABoCgCDgBFEXAAKIqAA0BRBBwAiiLgAFAUAQeAogg4ABRFwAGgKAIOAEURcAAoioADQFEEHACKIuAAUBQBB4CiCDgAFEXAAaCobn4n5kS4Zfeqzl2YGfcYADAxygT83IUZLR7ZP+4xRmrv4VPjHgHABOMQCgAURcABoCgCDgBFEXAAKIqAA0BRBBwAiiLgAFAUAQeAogg4ABRFwAGgqI4Bt32T7RdtL9l+zfaDzfr1tk/Yfr253D78cQEAa7p5BX5Z0sNJPi7pTkn3275N0iOSTia5VdLJ5jYAYEQ6BjzJxSSvNNfflbQkaZekuyUdbx52XNI9Q5oRALCBLR0Dtz0n6XZJL0u6MclFqRV5STcMfDoAwKa6DrjtayU9I+mhJO9s4fsO2V6wvbCystLLjACADXQVcNtXqxXvJ5M82yxfsr2zuX+npOWNvjfJ0STzSeZnZ2cHMTMAQN19CsWSHpe0lOSxtrtekHSwuX5Q0vODHw8AsJlufiPPPkn3SXrV9ulm7VFJ35T0tO0vSzon6UtDmRAAsKGOAU/yI0ne5O7PDHYcAEC3OBMTAIoi4ABQFAEHgKIIOAAURcABoCgCDgBFEXAAKIqAA0BRBBwAiiLgAFBUN/8WCjAy12xblT0z7jFG6uZdq3rj/JW1ZwwGAcdEee/yjBaP7B/3GCO19/CpcY+AojiEAgBFEXAAKIqAA0BRBBwAiiLgAFAUAQeAogg4ABRFwAGgKAIOAEURcAAoioADQFEEHACKIuAAUBQBB4CiCDgAFEXAAaAoAg4ARRFwACiKgANAUR0DbvuY7WXbZ9rWvmH7gu3Tzdddwx0TALBeN6/An5B0YIP1byfZ03x9f7BjAQA66RjwJC9JensEswAAtqCfY+AP2P5xc4hl+2YPsn3I9oLthZWVlT6eDgDQrteAf0fSRyXtkXRR0rc2e2CSo0nmk8zPzs72+HQAgPV6CniSS0neT/KBpO9KumOwYwEAOukp4LZ3tt38oqQzmz0WADAc2zo9wPZTkvZL2mH7vKSvS9pve4+kSDor6avDGxEAsJGOAU9y7wbLjw9hFgDAFnAmJgAURcABoCgCDgBFEXAAKIqAA0BRBBwAiiLgAFAUAQeAogg4ABRFwAGgKAIOAEURcAAoioADQFEEHACKIuAAUBQBB4CiCDgAFEXAAaAoAg4ARRFwACiKgANAUQQcAIoi4ABQFAEHgKIIOAAURcABoCgCDgBFEXAAKIqAA0BRBBwAiiLgAFBUx4DbPmZ72faZtrXrbZ+w/XpzuX24YwIA1uvmFfgTkg6sW3tE0skkt0o62dwGAIxQx4AneUnS2+uW75Z0vLl+XNI9gx0LANBJr8fAb0xyUZKayxs2e6DtQ7YXbC+srKz0+HQAgPWG/iZmkqNJ5pPMz87ODvvpAOCK0WvAL9neKUnN5fLgRgIAdKPXgL8g6WBz/aCk5wczDgCgW918jPApSf8u6WO2z9v+sqRvSvqs7dclfba5DQAYoW2dHpDk3k3u+syAZwEAbAFnYgJAUQQcAIoi4ABQFAEHgKIIOAAURcABoCgCDgBFEXAAKIqAA0BRBBwAiup4Kj2A4bpm26rsmXGPMVI371rVG+evrD0PAwEHxuy9yzNaPLJ/3GOM1N7Dp8Y9wlTgEAoAFEXAAaAoAg4ARRFwACiKgANAUQQcAIoi4ABQFAEHgKIIOAAURcABoCgCDgBFEXAAKIqAA0BRBBwAiiLgAFAUAQeAogg4ABRFwAGgKAIOAEX19TsxbZ+V9K6k9yVdTjI/iKEAAJ0N4pcafyrJWwP4OQCALeAQCgAU1W/AI+kHthdtH9roAbYP2V6wvbCystLn0wEA1vQb8H1Jfk/S5yXdb/sP1z8gydEk80nmZ2dn+3w6AMCavgKe5M3mclnSc5LuGMRQAIDOeg647Y/Yvm7tuqTPSTozqMEAAB+un0+h3CjpOdtrP+d7Sf5lIFMBADrqOeBJfi7pkwOcBQCwBXyMEACKIuAAUNQgzsQEgC25Ztuq7JlxjzFSN+9a1RvnB7tnAg5g5N67PKPFI/vHPcZI7T18auA/k0MoAFAUAQeAogg4ABRFwAGgKAIOAEURcAAoioADQFEEHACKIuAAUBQBB4CiCDgAFEXAAaAoAg4ARRFwACiKgANAUQQcAIoi4ABQFAEHgKIIOAAURcABoCgCDgBFEXAAKIqAA0BRBBwAiiLgAFAUAQeAogg4ABTVV8BtH7D9U9s/s/3IoIYCAHTWc8BtXyXp7yR9XtJtku61fdugBgMAfLh+XoHfIelnSX6e5D1J/yjp7sGMBQDoxEl6+0b7TyUdSPKV5vZ9kn4/yQPrHndI0qHm5sck/bSLH79D0ls9DTb52Ftd07w/9jbZbkkyu35xWx8/0Bus/crfBkmOSjq6pR9sLySZ73WwScbe6prm/bG3mvo5hHJe0k1tt3dLerO/cQAA3eon4P8p6Vbbv237Gkl/JumFwYwFAOik50MoSS7bfkDSv0q6StKxJK8NaK4tHXIphr3VNc37Y28F9fwmJgBgvDgTEwCKIuAAUNREBXzaTs23fcz2su0zbWvX2z5h+/Xmcvs4Z+yV7Ztsv2h7yfZrth9s1svvz/av2/4P2//d7O2vmvXye1tj+yrb/2X7n5vb07S3s7ZftX3a9kKzNjX7azcxAZ/SU/OfkHRg3dojkk4muVXSyeZ2RZclPZzk45LulHR/8+c1DftblfTpJJ+UtEfSAdt3ajr2tuZBSUttt6dpb5L0qSR72j7/PW37kzRBAdcUnpqf5CVJb69bvlvS8eb6cUn3jHKmQUlyMckrzfV31YrBLk3B/tLyv83Nq5uvaAr2Jkm2d0v6Y0l/37Y8FXv7EFO5v0kK+C5J/9N2+3yzNm1uTHJRakVQ0g1jnqdvtuck3S7pZU3J/ppDDKclLUs6kWRq9ibpbyX9haQP2tamZW9S6y/bH9hebP4pD2m69vdL/ZxKP2hdnZqPyWL7WknPSHooyTv2Rn+M9SR5X9Ie278p6TnbvzvmkQbC9hckLSdZtL1/zOMMy74kb9q+QdIJ2z8Z90DDMkmvwK+UU/Mv2d4pSc3l8pjn6Zntq9WK95NJnm2Wp2Z/kpTkF5JOqfVexjTsbZ+kP7F9Vq3DlJ+2/Q+ajr1JkpK82VwuS3pOrcOzU7O/dpMU8Cvl1PwXJB1srh+U9PwYZ+mZWy+1H5e0lOSxtrvK78/2bPPKW7Z/Q9IfSfqJpmBvSf4yye4kc2r9P/ZvSf5cU7A3SbL9EdvXrV2X9DlJZzQl+1tvos7EtH2XWsfn1k7NPzLeifpj+ylJ+9X65ywvSfq6pH+S9LSkmyWdk/SlJOvf6Jx4tv9A0g8lvar/P5b6qFrHwUvvz/Yn1Hqj6yq1XuQ8neSvbf+Wiu+tXXMI5WtJvjAte7P9O2q96pZah4i/l+TItOxvvYkKOACge5N0CAUAsAUEHACKIuAAUBQBB4CiCDgAFEXAAaAoAg4ARf0f48kwiswlyCEAAAAASUVORK5CYII=\n",
      "text/plain": [
       "<Figure size 432x288 with 1 Axes>"
      ]
     },
     "metadata": {
      "needs_background": "light"
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "plt.hist(df['phd'],facecolor =\"peru\",edgecolor =\"blue\",bins =5)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 41,
   "id": "0eec9854",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "{'whiskers': [<matplotlib.lines.Line2D at 0x1c72a821970>,\n",
       "  <matplotlib.lines.Line2D at 0x1c72a821cd0>],\n",
       " 'caps': [<matplotlib.lines.Line2D at 0x1c72a82d070>,\n",
       "  <matplotlib.lines.Line2D at 0x1c72a82d3d0>],\n",
       " 'boxes': [<matplotlib.lines.Line2D at 0x1c72a821610>],\n",
       " 'medians': [<matplotlib.lines.Line2D at 0x1c72a82d730>],\n",
       " 'fliers': [<matplotlib.lines.Line2D at 0x1c72a82da90>],\n",
       " 'means': []}"
      ]
     },
     "execution_count": 41,
     "metadata": {},
     "output_type": "execute_result"
    },
    {
     "data": {
      "image/png": "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\n",
      "text/plain": [
       "<Figure size 432x288 with 1 Axes>"
      ]
     },
     "metadata": {
      "needs_background": "light"
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "plt.boxplot(df['phd'],vert = True)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 43,
   "id": "cfe84afd",
   "metadata": {},
   "outputs": [
    {
     "ename": "AttributeError",
     "evalue": "module 'matplotlib.pyplot' has no attribute 'tile'",
     "output_type": "error",
     "traceback": [
      "\u001b[1;31m---------------------------------------------------------------------------\u001b[0m",
      "\u001b[1;31mAttributeError\u001b[0m                            Traceback (most recent call last)",
      "\u001b[1;32m<ipython-input-43-d3d5f03723c2>\u001b[0m in \u001b[0;36m<module>\u001b[1;34m\u001b[0m\n\u001b[1;32m----> 1\u001b[1;33m \u001b[0mplt\u001b[0m\u001b[1;33m.\u001b[0m\u001b[0mboxplot\u001b[0m\u001b[1;33m(\u001b[0m\u001b[0mdf\u001b[0m\u001b[1;33m[\u001b[0m\u001b[1;34m'phd'\u001b[0m\u001b[1;33m]\u001b[0m\u001b[1;33m,\u001b[0m\u001b[0mvert\u001b[0m \u001b[1;33m=\u001b[0m\u001b[1;32mFalse\u001b[0m\u001b[1;33m)\u001b[0m\u001b[1;33m;\u001b[0m\u001b[0mplt\u001b[0m\u001b[1;33m.\u001b[0m\u001b[0mylabel\u001b[0m\u001b[1;33m(\u001b[0m\u001b[1;34m'PHD'\u001b[0m\u001b[1;33m)\u001b[0m\u001b[1;33m;\u001b[0m\u001b[0mplt\u001b[0m\u001b[1;33m.\u001b[0m\u001b[0mxlabel\u001b[0m\u001b[1;33m(\u001b[0m\u001b[1;34m\"phd\"\u001b[0m\u001b[1;33m)\u001b[0m\u001b[1;33m;\u001b[0m\u001b[0mplt\u001b[0m\u001b[1;33m.\u001b[0m\u001b[0mtile\u001b[0m\u001b[1;33m(\u001b[0m\u001b[1;34m\"PHD\"\u001b[0m\u001b[1;33m)\u001b[0m\u001b[1;33m\u001b[0m\u001b[1;33m\u001b[0m\u001b[0m\n\u001b[0m",
      "\u001b[1;31mAttributeError\u001b[0m: module 'matplotlib.pyplot' has no attribute 'tile'"
     ]
    },
    {
     "data": {
      "image/png": "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\n",
      "text/plain": [
       "<Figure size 432x288 with 1 Axes>"
      ]
     },
     "metadata": {
      "needs_background": "light"
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "plt.boxplot(df['phd'],vert =False);plt.ylabel('PHD');plt.xlabel(\"phd\");plt.tile(\"PHD\")"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 44,
   "id": "408ffdf2",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "{'bodies': [<matplotlib.collections.PolyCollection at 0x1c72a9603a0>],\n",
       " 'cmaxes': <matplotlib.collections.LineCollection at 0x1c72a9601c0>,\n",
       " 'cmins': <matplotlib.collections.LineCollection at 0x1c72a960220>,\n",
       " 'cbars': <matplotlib.collections.LineCollection at 0x1c72a960850>}"
      ]
     },
     "execution_count": 44,
     "metadata": {},
     "output_type": "execute_result"
    },
    {
     "data": {
      "image/png": "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\n",
      "text/plain": [
       "<Figure size 432x288 with 1 Axes>"
      ]
     },
     "metadata": {
      "needs_background": "light"
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "plt.violinplot(df['service'])"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 45,
   "id": "556f8e67",
   "metadata": {},
   "outputs": [],
   "source": [
    "df = pd.DataFrame(index=['Aditya', 'Abbas', 'Cornelia', 'Stephanie', 'Monte'],\n",
    "                 data={'Apples':[20,10,40,20,50],'Oranges':[35,40,25,19,33]})"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 46,
   "id": "1946fb74",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>Apples</th>\n",
       "      <th>Oranges</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>Aditya</th>\n",
       "      <td>20</td>\n",
       "      <td>35</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Abbas</th>\n",
       "      <td>10</td>\n",
       "      <td>40</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Cornelia</th>\n",
       "      <td>40</td>\n",
       "      <td>25</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Stephanie</th>\n",
       "      <td>20</td>\n",
       "      <td>19</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Monte</th>\n",
       "      <td>50</td>\n",
       "      <td>33</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "           Apples  Oranges\n",
       "Aditya         20       35\n",
       "Abbas          10       40\n",
       "Cornelia       40       25\n",
       "Stephanie      20       19\n",
       "Monte          50       33"
      ]
     },
     "execution_count": 46,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 54,
   "id": "7aa722f9",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "iVBORw0KGgoAAAANSUhEUgAAA54AAAEhCAYAAAAXjH9uAAAAOXRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjMuNCwgaHR0cHM6Ly9tYXRwbG90bGliLm9yZy8QVMy6AAAACXBIWXMAAAsTAAALEwEAmpwYAAAgZElEQVR4nO3dfZiVdb3v8fdXQCdFURTcBiFoaAISwujW8vhEqLULtTJ8ysekOu1Sc3uivPZVVqfManeqU5pliVsFFSXn6Kl0K4QaxVOKcKHhsyAJ4hHFNHn4nj/WggZEmTUz99ysmffruuZa677vtWZ9Zq4lzmf9fvfvjsxEkiRJkqSibFd2AEmSJElS52bxlCRJkiQVyuIpSZIkSSqUxVOSJEmSVCiLpyRJkiSpUBZPSZIkSVKhunfki+2xxx45cODAjnxJSZIkSVIHmTt37guZ2Wfz/R1aPAcOHMicOXM68iUlSZIkSR0kIp7e0n6n2kqSJEmSCmXxlCRJkiQVyuIpSZIkSSpUh57jKUmSJEnbmjVr1rBkyRJef/31sqPUjYaGBvr370+PHj1a9HiLpyRJkqQubcmSJey8884MHDiQiCg7zjYvM1m5ciVLlixh0KBBLXpOi6baRsRTEfFwRDwYEXOq+3pHxN0Rsbh6u1sbskuSJElSKV5//XV23313S2cLRQS77757TSPEtZzjeXRmjsjMxur2BOCezBwM3FPdliRJkqS6Y+msTa2/r7YsLnQCMLF6fyJwYhu+lyRJkiR1aVOnTiUieOSRR1r9Pc4++2ymTJnSjqnaR0vP8UzgrohI4GeZeTWwZ2YuA8jMZRHRd0tPjIjxwHiAAQMGtENkSZIkSWXr169f2RFqsnTp0hY/tr1/tpa+9qRJkzj88MOZPHkyX/va19o1Q9laOuL5/swcCXwQ+FxEHNHSF8jMqzOzMTMb+/Tp06qQkiRJktSZrV69mgceeIBrrrmGyZMnAzB9+nSOOOIITjrpJIYMGcJnPvMZ1q9fD0DPnj25+OKLGTlyJKNHj2bFihVv+p5z587lyCOPZNSoURx33HEsW7YMgB/96EcMGTKE4cOHc8opp3TIz9ei4pmZz1VvlwNTgUOA5yNiL4Dq7fKiQkqSJElSZ/brX/+a448/nv3224/evXszb948AGbNmsX3v/99Hn74YR5//HFuu+02AF599VVGjhzJvHnzOPLII7nssss2+X5r1qzh85//PFOmTGHu3Lmce+65XHrppQBcfvnl/PnPf2b+/PlcddVVHfLzbbV4RsROEbHzhvvAscACoAk4q/qws4DbiwopSZIkSZ3ZpEmTNo4+nnLKKUyaNAmAQw45hH322Ydu3bpx6qmncv/99wOw3XbbMW7cOADOOOOMjfs3ePTRR1mwYAFjxoxhxIgRfPOb32TJkiUADB8+nNNPP53rr7+e7t075gqbLXmVPYGp1VWLugM3ZuZvI2I2cHNEnAc8A5xcXExJkiRJ6pxWrlzJvffey4IFC4gI1q1bR0TwoQ996E2rx77VarKb789Mhg4dysyZM9/02DvvvJMZM2bQ1NTEN77xDRYuXFh4Ad3qiGdmPpGZ761+Dc3M/1ndvzIzR2fm4Orti4UmlSRJkqROaMqUKZx55pk8/fTTPPXUUzz77LMMGjSI+++/n1mzZvHkk0+yfv16brrpJg4//HAA1q9fv3H12htvvHHj/g32339/VqxYsbF4rlmzhoULF7J+/XqeffZZjj76aK644gpeeuklVq9eXfjP2DHjqpIkSZKkLZo0aRITJkzYZN/HPvYxrrzySg477DAmTJjAww8/vHGhIYCddtqJhQsXMmrUKHr16sVNN920yfO33357pkyZwhe+8AVWrVrF2rVrufDCC9lvv/0444wzWLVqFZnJRRddxK677lr4zxiZWfiLbNDY2Jhz5szpsNeTJEmSVIzOdDmVRYsWccABB3RgmpaZPn063/ve97jjjjvedKxnz54dMlL5drb0e4uIuZnZuPljW3o5FUmSJEmSWsWptpIkSZK0DTrqqKM46qijtnis7NHOWjniKUmSJEkqlMVTkiRJklQoi6ckSZIkqVAWT0mSJElSoSyekiRJklSyJUuWcMIJJzB48GD23XdfLrjgAt54442yY7UbV7WVJEmSpGbGjh3brt+vqanpbY9nJh/96Ef57Gc/y+233866desYP348l156Kd/97nc3Pm7t2rV0716fFc4RT0mSJEkq0b333ktDQwPnnHMOAN26deMHP/gBv/zlL/npT3/KySefzEc+8hGOPfZYVq9ezejRoxk5ciQHHnggt99+OwBPPfUUBxxwAOeffz5Dhw7l2GOP5bXXXgNg9uzZDB8+nMMOO4xLLrmEYcOGAbBu3TouueQSDj74YIYPH87PfvYzAJYtW8YRRxzBiBEjGDZsGPfdd1+bf0aLpyRJkiSVaOHChYwaNWqTfbvssgsDBgxg7dq1zJw5k4kTJ24sqFOnTmXevHlMmzaNiy++mMwEYPHixXzuc59j4cKF7Lrrrtx6660AnHPOOVx11VXMnDmTbt26bXyNa665hl69ejF79mxmz57Nz3/+c5588kluvPFGjjvuOB588EEeeughRowY0eafsT7HaSVJkiSpk8hMIuIt948ZM4bevXtv3PeVr3yFGTNmsN1227F06VKef/55AAYNGrSxJI4aNYqnnnqKl156iVdeeYX3ve99AJx22mnccccdANx1113Mnz+fKVOmALBq1SoWL17MwQcfzLnnnsuaNWs48cQTLZ6SJEmSVO+GDh26cXRyg5dffplnn32Wbt26sdNOO23cf8MNN7BixQrmzp1Ljx49GDhwIK+//joAO+yww8bHdevWjddee23jaOiWZCY//vGPOe644950bMaMGdx555188pOf5JJLLuHMM89s08/oVFtJkiRJKtHo0aP529/+xnXXXQdUzr28+OKLOfvss9lxxx03eeyqVavo27cvPXr0YNq0aTz99NNv+7132203dt55Z/74xz8CMHny5I3HjjvuOK688krWrFkDwF/+8hdeffVVnn76afr27cv555/Peeedx7x589r8M1o8JUmSJKlEEcHUqVO55ZZbGDx4MPvttx8NDQ1861vfetNjTz/9dObMmUNjYyM33HAD73nPe7b6/a+55hrGjx/PYYcdRmbSq1cvAD71qU8xZMgQRo4cybBhw/j0pz/N2rVrmT59OiNGjOCggw7i1ltv5YILLmj7z/h2Q6/trbGxMefMmdNhrydJkiSpGP369Ss7Qk2WLl36lscWLVrEAQcc0IFpOtbq1avp2bMnAJdffjnLli3jhz/8YZu/75Z+bxExNzMbN3+s53hKkiRJUid255138u1vf5u1a9ey9957c+2113Z4BounJEmSJHVi48aNY9y4caVm8BxPSZIkSVKhLJ6SJEmSuryOXPumM6j192XxlCRJktSlNTQ0sHLlSstnC2UmK1eupKGhocXP8RxPSZIkSV1a//79WbJkCStWrCg7St1oaGigf//+LX68xVOSJElSl9ajRw8GDRpUdoxOzam2kiRJkqRCWTwlSZIkSYWyeEqSJEmSCmXxlCRJkiQV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\n",
      "text/plain": [
       "<Figure size 1152x288 with 1 Axes>"
      ]
     },
     "metadata": {
      "needs_background": "light"
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "color=['.2','.7']\n",
    "ax = df.plot.bar(color=['.1','.3'],figsize=(16,4))"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 51,
   "id": "b0c92236",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "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\n",
      "text/plain": [
       "<Figure size 1152x288 with 1 Axes>"
      ]
     },
     "metadata": {
      "needs_background": "light"
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "ax = df.plot.kde(color=['.2',\".7\"], figsize=(16,4))"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 55,
   "id": "7b9dbbde",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "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\n",
      "text/plain": [
       "<Figure size 1224x1224 with 3 Axes>"
      ]
     },
     "metadata": {
      "needs_background": "light"
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "fig, (ax1, ax2, ax3) = plt.subplots(1,3, figsize=(17,17))"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "465de78c",
   "metadata": {},
   "outputs": [],
   "source": []
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "12137647",
   "metadata": {},
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.8.8"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}
