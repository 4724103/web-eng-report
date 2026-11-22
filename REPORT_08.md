# 第8回 Webエンジニアリング演習 レポート
## 学籍番号
4724103
## コンポーネント構成
App
└── src/
　　├── main.tsx
　　└── App.tsx 
　  └── TodoList
　　├── TodoItem
## `TodoItem`のProps型
import type { Todo } from "../types";

type TodoItemProps = {
    todo: Todo;
};

export function TodoItem({ todo }: TodoItemProps) {
    return (
        <li>
            <strong>{todo.title}</strong>
            <span> {todo.completed ? "(完了)" : "(未完了)"}</span>
            {todo.dueDate && <span> 期限: {todo.dueDate}</span>}
        </li>
    );
}

## 期限あり・なしの画面確認結果
import type { Todo } from "./types";

export const todos: Todo[] = [
    { id: 1, title: "Reactを学ぶ", completed: true },
    { id: 2, title: "Propsを確認する", dueDate:"11/23", completed: false },
    { id: 3, title: "Stateを更新する", completed: false },
];