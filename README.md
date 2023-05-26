 private void button1_Click(object sender, EventArgs e)
        {
            Cars cars = new Cars();
            cars.ShowDialog();
        }

        private void button2_Click(object sender, EventArgs e)
        {
            Rates rates = new Rates();
            rates.ShowDialog();
        }

        private void button3_Click(object sender, EventArgs e)
        {
            Rental rental = new Rental();
            rental.ShowDialog();
        }

        private void button4_Click(object sender, EventArgs e)
        {
            Clients clients = new Clients();
            clients.ShowDialog();
        }

        private void button5_Click(object sender, EventArgs e)
        {
            PersonalCheck personal_check = new PersonalCheck();
            personal_check.ShowDialog();
        }

        private void button6_Click(object sender, EventArgs e)
        {
            this.Close();
            Application.Exit();
        }

        private void MainScreen_FormClosed(object sender, FormClosedEventArgs e)
        {
            Application.Exit();
        }
        
        ################# Cars #####################
                public Cars()
        {
            InitializeComponent();
        }

        private void Cars_Load(object sender, EventArgs e)
        {
            // TODO: данная строка кода позволяет загрузить данные в таблицу "avtoprokatDataSet.Автомобиль". При необходимости она может быть перемещена или удалена.
            this.автомобильTableAdapter.Fill(this.avtoprokatDataSet.Автомобиль);

        }

        private void label1_Click(object sender, EventArgs e)
        {

        }

        private void label2_Click(object sender, EventArgs e)
        {

        }

        private void label15_Click(object sender, EventArgs e)
        {

        }

        private void button1_Click(object sender, EventArgs e)
        {
            автомобильBindingSource.MovePrevious();
        }

        private void button2_Click(object sender, EventArgs e)
        {
            автомобильBindingSource.AddNew();
        }

        private void button3_Click(object sender, EventArgs e)
        {
            this.Validate();
            this.автомобильBindingSource.EndEdit();
            this.tableAdapterManager.UpdateAll(this.avtoprokatDataSet);
        }

        private void button4_Click(object sender, EventArgs e)
        {
            автомобильBindingSource.RemoveCurrent();
        }

        private void button5_Click(object sender, EventArgs e)
        {
            автомобильBindingSource.MoveNext();
        }

        private void button6_Click(object sender, EventArgs e)
        {
            this.Close();
        }
        
