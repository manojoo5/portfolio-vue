<template>
  <ul role="list" class="divide-y divide-gray-100 px-32 mt-14">
    <li v-for="person in people" :key="person.email" class="flex justify-between gap-x-6 py-5">
      <div class="flex min-w-0 gap-x-4">
        <img class="h-12 w-12 flex-none rounded-full bg-gray-50" :src="person.imageUrl" alt="" />
        <div class="min-w-0 flex-auto">
          <p class="text-sm font-semibold leading-6 text-gray-900">{{ person.name }}</p>
          <p class="mt-1 truncate text-xs leading-5 text-gray-500">{{ person.email }}</p>
        </div>
      </div>
      <div class="hidden shrink-0 sm:flex sm:flex-col sm:items-end">
        <p class="text-sm leading-6 text-gray-900">{{ person.role }}</p>
        <p v-if="person.lastSeen" class="mt-1 text-xs leading-5 text-gray-500">
          Last seen <time :datetime="person.lastSeenDateTime">{{ person.lastSeen }}</time>
        </p>
        <div v-else class="mt-1 flex items-center gap-x-1.5">
          <div class="flex-none rounded-full bg-emerald-500/20 p-1">
            <div class="h-1.5 w-1.5 rounded-full bg-emerald-500" />
          </div>
          <p class="text-xs leading-5 text-gray-500">Online</p>
        </div>
      </div>
    </li>
  </ul>
</template>

<script setup>
const people = [
  {
    name: 'Custom software development',
    email: 'manojkumarv085@gmail.com',
    role: 'Co-Founder / CEO',
    imageUrl:
      'https://media.licdn.com/dms/image/D4D03AQGoga14BBlu6A/profile-displayphoto-shrink_200_200/0/1691265565915?e=1699488000&v=beta&t=DP5rXdVCm6oLKIQMDkBqsFcL25VnL4578-RZ8QIURaQ',
    lastSeen: '3h ago',
    lastSeenDateTime: '2023-01-23T13:23Z',
  },
  {
    name: 'Mobile software development',
    email: 'manojkumarv085@gmail.com',
    role: 'Co-Founder / CTO',
    imageUrl:
      'https://media.licdn.com/dms/image/D4D03AQGoga14BBlu6A/profile-displayphoto-shrink_200_200/0/1691265565915?e=1699488000&v=beta&t=DP5rXdVCm6oLKIQMDkBqsFcL25VnL4578-RZ8QIURaQ',
    lastSeen: '3h ago',
    lastSeenDateTime: '2023-01-23T13:23Z',
  },
  {
    name: 'Web development',
    email: 'manojkumarv085@gmail.com',
    role: 'Business Relations',
    imageUrl:
      'https://media.licdn.com/dms/image/D4D03AQGoga14BBlu6A/profile-displayphoto-shrink_200_200/0/1691265565915?e=1699488000&v=beta&t=DP5rXdVCm6oLKIQMDkBqsFcL25VnL4578-RZ8QIURaQ',
    lastSeen: null,
  },
  {
    name: 'Cloud software development',
    email: 'manojkumarv085@gmail.com',
    role: 'Designer',
    imageUrl:
      'https://media.licdn.com/dms/image/D4D03AQGoga14BBlu6A/profile-displayphoto-shrink_200_200/0/1691265565915?e=1699488000&v=beta&t=DP5rXdVCm6oLKIQMDkBqsFcL25VnL4578-RZ8QIURaQ',
    lastSeen: '3h ago',
    lastSeenDateTime: '2023-01-23T13:23Z',
  },
  {
    name: 'Content Management System (CMS)',
    email: 'manojkumarv085@gmail.com',
    role: 'Front-end Developer',
    imageUrl:
      'https://media.licdn.com/dms/image/D4D03AQGoga14BBlu6A/profile-displayphoto-shrink_200_200/0/1691265565915?e=1699488000&v=beta&t=DP5rXdVCm6oLKIQMDkBqsFcL25VnL4578-RZ8QIURaQ',
    lastSeen: '3h ago',
    lastSeenDateTime: '2023-01-23T13:23Z',
  },
  {
    name: 'System integration',
    email: 'manojkumarv085@gmail.com',
    role: 'Director of Product',
    imageUrl:
      'https://media.licdn.com/dms/image/D4D03AQGoga14BBlu6A/profile-displayphoto-shrink_200_200/0/1691265565915?e=1699488000&v=beta&t=DP5rXdVCm6oLKIQMDkBqsFcL25VnL4578-RZ8QIURaQ',
    lastSeen: null,
  },
  {
    name: 'DevOps',
    email: 'manojkumarv085@gmail.com',
    role: 'Director of Product',
    imageUrl:
      'https://media.licdn.com/dms/image/D4D03AQGoga14BBlu6A/profile-displayphoto-shrink_200_200/0/1691265565915?e=1699488000&v=beta&t=DP5rXdVCm6oLKIQMDkBqsFcL25VnL4578-RZ8QIURaQ',
    lastSeen: null,
  },
  {
    name: 'E-commerce software development',
    email: 'manojkumarv085@gmail.com',
    role: 'Director of Product',
    imageUrl:
      'https://media.licdn.com/dms/image/D4D03AQGoga14BBlu6A/profile-displayphoto-shrink_200_200/0/1691265565915?e=1699488000&v=beta&t=DP5rXdVCm6oLKIQMDkBqsFcL25VnL4578-RZ8QIURaQ',
    lastSeen: null,
  },
  {
    name: 'Database development',
    email: 'manojkumarv085@gmail.com',
    role: 'Director of Product',
    imageUrl:
      'https://media.licdn.com/dms/image/D4D03AQGoga14BBlu6A/profile-displayphoto-shrink_200_200/0/1691265565915?e=1699488000&v=beta&t=DP5rXdVCm6oLKIQMDkBqsFcL25VnL4578-RZ8QIURaQ',
    lastSeen: null,
  },
  {
    name: 'Enterprise software development',
    email: 'manojkumarv085@gmail.com',
    role: 'Director of Product',
    imageUrl:
      'https://media.licdn.com/dms/image/D4D03AQGoga14BBlu6A/profile-displayphoto-shrink_200_200/0/1691265565915?e=1699488000&v=beta&t=DP5rXdVCm6oLKIQMDkBqsFcL25VnL4578-RZ8QIURaQ',
    lastSeen: null,
  },
  {
    name: 'System integration',
    email: 'manojkumarv085@gmail.com',
    role: 'Director of Product',
    imageUrl:
      'https://media.licdn.com/dms/image/D4D03AQGoga14BBlu6A/profile-displayphoto-shrink_200_200/0/1691265565915?e=1699488000&v=beta&t=DP5rXdVCm6oLKIQMDkBqsFcL25VnL4578-RZ8QIURaQ',
    lastSeen: null,
  },
]
</script>