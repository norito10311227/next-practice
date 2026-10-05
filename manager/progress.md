# 進捗ログ

最終更新：2026-10-05（Claude Code セッション、`next-practice` リポジトリ）

## 【重要】マネージャー設定ファイルが一度消失していた

2026-09-27にCLAUDE.md・manager/・.claude/を設置し、GitHubにpush済みと判断していたが、**2026-10-05に確認したところ、このリポジトリにはCLAUDE.md・manager/・.claude/が一切存在せず、gitの履歴にも一度も記録がなかった**（原因不明。`git status`だけで「push済み」と判断し、`git log -- <path>`で実際の履歴を確認していなかったことが一因）。今回、`react-practice`から再設置した。**今後は、設置直後に必ず`git log --oneline -- CLAUDE.md manager/`等でコミット履歴そのものを確認すること。** `AGENTS.md`（Next.js自動生成）も消えていた（再生成待ち）。

## 現在地

- `next-practice`は、Udemy講座の前半で学んだ要素（Server Actions、Middleware、Route Handler、`dynamic`設定など）を**個別に試すための実験用リポジトリ**として使われている。
- 本格的なタスク管理アプリ（CRUD・MongoDB連携・優先度機能）は、**別リポジトリ`next-practice-app`**で実装中（そちらの`manager/progress.md`を参照）。
- 現在のブランチに未コミットの変更が複数あり（`src/app/sa/page.jsx`、`src/middleware.ts`、`src/app/api/tasks/route.ts`、`src/app/cc/page.tsx`、`src/app/sc/page.tsx`等）、学習者が様々な実験をしている状態。

## このリポジトリで扱った内容（2026-09-28〜10月上旬）

- Server Actions基礎：`'use server'`/`'use client'`の境界、`useFormState`/`useFormStatus`、`.bind()`で引数を事前固定する仕組み、`FormData`の自動収集、型チェックが素通りする`any`絡みのタイポ（`json.error` vs `json.errors`）。
- Middleware：`export const middleware`（命名を厳密に要求される。`middleWare`のような大文字小文字違いでNext.jsがエラーを出した実例あり）。
- Route Handler（`NextRequest`/`NextResponse`）と、`export const dynamic = 'force-dynamic'`によるキャッシュ制御。
- VS Codeのトラブルシューティング実例：TypeScriptのワークスペース版と内蔵版の違い（Select TypeScript Version → Use Workspace Version）、`.next`フォルダが壊れたときは削除して再生成させる、エディタの赤線は実害のない場合がある（`@tailwind`のUnknown at ruleなど）。

## 保留事項（学習者から回収するもの）

- [ ] 研究室見学のアポ（香山研・小林研・北研）と日程 → **期限：2026年12月末までに最低1件**
- [ ] 研究室配属の時期、推薦特別選抜の学科内基準

## マネージャーの保留タスク

- [ ] 2026年11月：信州大 2028年4月入学（改組後）入試の予告を確認
- [ ] 2026年12月末：研究室見学アポの状況を確認
- [ ] 2027年1月：IPA の CBT 再開時期と新制度を確認し、FE／CS基礎の方針を決める
- [ ] 現在の学習の主戦場は`next-practice-app`。こちらのリポジトリの今後の使い道（実験用のまま残すか）は未確定。

## 次にやること

- 現在の主な作業は`next-practice-app`側（W6：自力実装の演習中）。詳細はそちらの`manager/progress.md`参照。
- このリポジトリの未コミットの変更は、学習者自身のタイミングでcommit/pushする。
