// Масив користувачів
const users = [
  { id: 1, name: 'Олександр', age: 28 },
  { id: 2, name: 'Марія', age: 32 },
  { id: 3, name: 'Іван', age: 22 },
  { id: 4, name: 'Анна', age: 27 }
];

// Функція для симуляції затримки (імітуючи асинхронний запит)
function fetchUserData(userId) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      const user = users.find(u => u.id === userId);
      if (user) {
        resolve(user);
      } else {
        reject('Користувача не знайдено');
      }
    }, 1000);
  });
}

// Функція для обробки отриманих даних
async function getUserInfo(userId) {
  try {
    const user = await fetchUserData(userId);
    console.log(`Користувач знайдений: ${user.name}, вік: ${user.age}`);
  } catch (error) {
    console.error(error);
  }
}

// Приклад виклику асинхронної функції
getUserInfo(3); // Успішний запит
getUserInfo(5); // Помилка: Користувача не знайдено

// Функція для фільтрації користувачів за віком
const getUsersByAge = (ageLimit) => {
  return users.filter(user => user.age >= ageLimit);
};

console.log(getUsersByAge(30)); // Виведе список користувачів старше 30 років
