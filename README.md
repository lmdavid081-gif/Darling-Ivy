
.buttons {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 14px;
  margin-top: 25px;
}

#yes {
  display: block;
  width: 90%;
  padding: 18px;
  font-size: 20px;
  font-weight: 900;
  color: white;
  background: linear-gradient(135deg, #fe2c55, #ff6933);
  border: 2px solid #ff8750;
  border-radius: 18px;
  box-shadow: 0 0 22px #fe2c5570;
  cursor: pointer;
  animation: yesPulse 1.2s infinite alternate;
}

#no {
  padding: 10px 18px;
  font-size: 13px;
  color: #aaa;
  background: #292929;
  border-radius: 20px;
  cursor: pointer;
}

@keyframes yesPulse {
  from {
    transform: scale(1);
    box-shadow: 0 0 12px #fe2c5540;
  }
  to {
    transform: scale(1.04);
    box-shadow: 0 0 25px #fe2c55a0;
  }
}
