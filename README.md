# SmartMCQ Generator

## ☁️ AWS EC2 Setup (Step-by-Step)
1. Login to AWS Console: https://aws.amazon.com/console/

2. Create an EC2 Instance

Search for EC2

Launch a new instance

Choose Ubuntu (20.04 or 22.04 LTS)

Select instance type (e.g., t2.micro for testing)

Create or select a key pair

Configure Security Group:

Allow SSH (22)

Allow Custom TCP → Port 8501 (Streamlit)


3. you need to config the UBUNTU Machine
Connect to Your EC2 Instance
#bash
ssh -i your-key.pem ubuntu@your-ec2-public-ip

4. launch the instance

5. update the machine:

sudo apt update

sudo apt-get update

sudo apt upgrade -y

6. Install Required Packages
sudo apt install git curl unzip tar make sudo vim wget -y

7. Clone the Repository
git clone "Your-repository"
cd YOUR_REPOSITORY_NAME

8. Install Python Dependencies
sudo apt install python3-pip

pip3 install -r requirements.txt

python3 -m streamlit run StreamlitAPP.py

##### (Optional) Add OpenAI API Key

1. create .env file in your server
touch .env
vi .env

#Press i (insert mode), then add:

OPENAI_API_KEY=your_openai_api_key_here

Press Esc, then type:

:wq

and hit Enter.

▶️ Run the Application
9️⃣ Start Streamlit App
python3 -m streamlit run StreamlitAPP.py


## 🌐 Access the App

Open your browser:

http://YOUR_EC2_PUBLIC_IP:8501

🔐 Security Group Configuration

Ensure your EC2 Security Group has:

Inbound Rule

Type: Custom TCP

Port: 8501

Source: 0.0.0.0/0 (or your IP for security)# quizforge-ai
