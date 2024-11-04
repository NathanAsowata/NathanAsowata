### Hi, I'm Nathan,

You can visit my portfolio website at [nathanasowata.com](https://www.nathanasowata.com) or reach me directly on [LinkedIn](https://www.linkedin.com/in/nathanasowata/).



SqlConnection con;
public DAO(){
    con = new SqlConnection(ConfigurationManager.ConnectionStrings["DBCon"].ConnectionString);}
public SqlConnection OpenCon()
{    if (con.State == ConnectionState.Broken || con.State == ConnectionState.Closed)
    {        con.Open();
    }
    return con;}
public void CloseCon()

{
    if (con != null)    {
        if (con.State == ConnectionState.Open)        {
            con.Close();        }
    }}
