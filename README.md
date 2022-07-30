# Schedule_EngAll

원티드 프리온보딩 기업과제 Week-4-2

# 구성원

| 이름   |       팀 구성       |  기능 구현 및 역할   |
| ------ | :-----------------: | :------------------: |
| 이상지 | 팀장 </br> Frontend | React Query API 구현 |
| 김수빈 | 팀원 </br> Frontend |                      |
| 김민주 | 팀원 </br> Frontend |                      |

# 기술 스택

`React.js`
`TypeScript`
</br>

`React-Query`
`recoil`
`axois`
`json-server`
`SCSS`

</br>
</br>

# 폴더구조

```

```

</br>

# 실행 방법

</br>

# 상세 구현 설명

## API

- src / index.ts
  - react-query 초기세팅
- httpRequest.ts
  - axios를 사용해 get, post, delete로직 구현
- ScheduleTable.tsx

  - react-query get, delete 구현
  - delete -> useMutation사용

  ```ts
  const queryClient = useQueryClient();

  const { data } = useQuery<Schedule[] | any>(['schedule'], () =>
    getSchedule()
  );

  const deleteMutation = useMutation((id: number) => deleteSchedule(id), {
    onSuccess: () => {
      queryClient.invalidateQueries(['schedule']);
    },
  });
  ```

```


```
