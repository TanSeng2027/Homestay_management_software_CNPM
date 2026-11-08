# Cấu trúc thư mục hiện tại
homestay-goc-nho/
├─ CONVENTIONS.md            # file này
├─ README.md                 # cách cài đặt và chạy
├─ server/
│  ├─ .env.example           # mẫu biến môi trường, KHÔNG commit .env
│  ├─ database/
│  │  ├─ schema.sql          # tạo 40 bảng theo PDM
│  │  └─ seed.sql            # vai trò, chức năng, quyền, tham số, dữ liệu mẫu
│  ├─ src/
│  │  ├─ app.js              # khởi tạo Express, gắn route và middleware
│  │  ├─ config/             # db.js, env.js
│  │  ├─ routes/             # <module>.routes.js
│  │  ├─ middlewares/        # auth.js, can.js, validate.js, errorHandler.js
│  │  ├─ validators/         # <module>.schema.js (joi)
│  │  ├─ controllers/        # <module>.controller.js
│  │  ├─ services/           # <module>.service.js – quy tắc nghiệp vụ
│  │  ├─ models/             # mỗi bảng PDM một model
│  │  ├─ constants/          # status.js, errorCodes.js, permissions.js
│  │  └─ utils/              # AppError.js, money.js, date.js, codeGenerator.js
│  └─ tests/                 # <module>.service.test.js
└─ client/
   ├─ .env.example           # VITE_API_URL
   └─ src/
      ├─ main.jsx, App.jsx
      ├─ routes/             # AppRoutes.jsx, ProtectedRoute.jsx
      ├─ layouts/            # CustomerLayout.jsx, StaffLayout.jsx
      ├─ pages/
      │  ├─ customer/        # MH06HomePage.jsx, MH08BookingPage.jsx …
      │  ├─ reception/       # MH15RoomBoardPage.jsx, MH16CheckInPage.jsx …
      │  ├─ housekeeping/    # MH19CleaningPage.jsx …
      │  ├─ service/         # MH18ServiceRecordPage.jsx
      │  ├─ manager/         # MH22ApprovalPage.jsx …
      │  ├─ accountant/      # MH23TransactionPage.jsx …
      │  ├─ admin/           # MH04UserPage.jsx …
      │  └─ common/          # MH01LoginPage.jsx, NotFoundPage.jsx …
      ├─ components/         # Button, Input, Table, Badge, Modal, Toast, Stepper …
      ├─ services/           # api.js (axios), bookingApi.js, stayApi.js …
      ├─ context/            # AuthContext.jsx
      ├─ hooks/              # useAuth.js, useFetch.js
      ├─ constants/          # status.js, errorMessages.js, menu.js
      ├─ utils/              # formatMoney.js, formatDate.js
      └─ styles/             # tokens.css (màu, font), global.css